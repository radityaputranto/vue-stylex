<template>
  <div id="app">
    <div>
      <img alt="Vue logo" src="./assets/logo.png" />
      <img alt="Vue logo" src="./assets/stylex-logo.png" />
    </div>
    <HelloWorld msg="Vue.js with StyleX CSS" />
  </div>
</template>

<script>
import HelloWorld from "./components/HelloWorld.vue";

export default {
  name: "App",
  components: {
    HelloWorld,
  },
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
