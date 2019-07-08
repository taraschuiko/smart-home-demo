<template>
  <div id="app">
    <div class="container">
      <Header />
      <Home />
    </div>
  </div>
</template>

<script>
import Header from "./components/Header";
import Home from "./components/Home.vue";

export default {
  name: "App",
  components: {
    Header,
    Home
  }
};
</script>

<style lang="scss">
#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  width: 100%;

  .container {
    overflow-x: scroll;
    height: 100%;
    padding: 8px;
  }
}
</style>
