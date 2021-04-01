<template>
  <div>
    <div class="card-holder">
      <div class="flex">
        <!-- Logo here-->
        <div>
        <img src="@/assets/img/logo.svg" height="16.63" width="95.34" alt="logo">
        </div>

        <!-- Visibility Toggler here-->
        <div class="ml-auto">
        
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "card",

  data: () => ({}),
};
</script>

<style scoped>
.card-holder {
  background: var(--primary-black);
  padding: 20px 15px 10px 15px;
  border-radius: 20px;
  }
</style>
