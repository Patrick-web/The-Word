<template>
  <div id="app">
    <main-layout />
  </div>
</template>

<script>
import MainLayout from "./components/MainLayout.vue";

export default {
  components: { MainLayout },
};
</script>

<style>
@import url("./assets/css/global.css");
@import url("./assets/css/animate.css");
#app {
  height: 100vh;
  width: 100vw;
  overflow: hidden;
  background: var(--appBackgroundColor);
}
</style>