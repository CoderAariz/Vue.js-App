<template>
  <div id="app">
    <HelloWorld msg="Welcome to FLIBO" />
  </div>
</template>

<script>
import HelloWorld from "./components/HelloWorld.vue";

export default {
  name: "App",
  components: {
    HelloWorld
  }
};
</script>

<style lang="scss">
#app {
  font-family: Georgia, "Times New Roman", Times, serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  font-size: 45px;
  color: rgb(195, 241, 28);
  margin-top: 0px;
  background-image: url("./assets/back.jpg");
  background-size: cover;
  background-repeat: no-repeat;
  background-attachment: fixed;
}
</style>
