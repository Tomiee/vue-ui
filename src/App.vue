<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png">
    <!-- <HelloWorld msg="Welcome to Your Vue.js App"/> -->
    <u-Button iconPosition="right" icon = 'loading'>按钮</u-Button>
  </div>
</template>



<script>
import HelloWorld from "./components/HelloWorld.vue";
import Button from "./components/Button";

export default {
  name: "app",
  components: {
    HelloWorld,
    "u-Button": Button
  },  
};
</script>

<style>
.icon {
  width: 1em;
  height: 1em;
  vertical-align: -0.15em;
  fill: black;
  overflow: hidden;
}

#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
