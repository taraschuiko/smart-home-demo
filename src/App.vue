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
@font-face {
  font-family: icons;
  src: url("./assets/icons.woff");
}

#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  width: 100%;

  .icon {
    font-family: icons;
    margin-right: 8px;
    font-size: 18px;
  }

  .container {
    overflow-x: scroll;
    height: 100%;
    padding: 8px;
  }
}
</style>
