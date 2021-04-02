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

.center {
  width: 499px;
  height: 305px;
  margin: 50px auto;
  padding: 0px 10px;
}
</style>
