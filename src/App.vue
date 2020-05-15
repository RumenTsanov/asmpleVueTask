<template>
  <div id="app">
    <MainComponent />
    <RecoveryCloudComponent />
    <!-- <BackupAndRestoreComponent /> -->
  </div>
</template>

<script>
import MainComponent from "./components/MainComponent.vue";
import RecoveryCloudComponent from "./components/RecoveryCloudComponent";
// import BackupAndRestoreComponent from "./components/BackupAndRestoreComponent";

export default {
  name: "App",
  components: {
    MainComponent,
    RecoveryCloudComponent
    // BackupAndRestoreComponent
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
