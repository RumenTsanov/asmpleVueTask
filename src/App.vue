<template>
  <div id="app">
    <MainComponent />
    <RecoveryCloudComponent />
  </div>
</template>

<script>
import MainComponent from "./components/MainComponent.vue";
import RecoveryCloudComponent from "./components/RecoveryCloudComponent";

export default {
  name: "App",
  components: {
    MainComponent,
    RecoveryCloudComponent
  }
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
