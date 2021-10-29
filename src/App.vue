<template>
  <div id="app">
    <ToDo />
    <!-- <img alt="Vue logo" src="./assets/logo.png" /> -->
    <!-- <HelloWorld msg="Welcome to Your Vue.js App" /> -->
  </div>
</template>

<script>
// import HelloWorld from "./components/HelloWorld.vue";
import ToDo from "./components/ToDo.vue";

export default {
  name: "App",
  components: {
    // HelloWorld,
    ToDo,
  },
};
</script>

<style lang="scss">
body {
  background: #a42d01;
  background: -moz-linear-gradient(left, #a42d01 0%, #f15e16 50%, #ce510d 100%);
  background: -webkit-linear-gradient(
    left,
    #a42d01 0%,
    #f15e16 50%,
    #ce510d 100%
  );
  background: linear-gradient(to right, #a42d01 0%, #f15e16 50%, #ce510d 100%);
}
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;

  color: #2c3e50;
  margin-top: 60px;
}
</style>
