<template>
  <div id="app">
    <div class="center">
      <card />
    </div>
  </div>
</template>

<script>
import card from "./components/card";

export default {
  name: "App",
  components: {
    card,
  },
};
</script>

<style>
#app {
  font-family: "Graphik";
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
}

.center{
 width: 499px;
height: 305px;
        position: absolute; /*Can also be `fixed`*/
        left: 0;
        right: 0;
        top: 0;
        bottom: 0;
        margin: auto;

       
}
</style>
