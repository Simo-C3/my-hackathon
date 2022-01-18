<template>
  <vue100vh :css="{ height: '100rvh' }" id="app">
    <Header />
    <router-view />
    <Footer />
  </vue100vh>
</template>

<script>
import vue100vh from "vue-100vh";

import Header from "./components/Header.vue";
import Footer from "./components/Footer.vue";

export default {
  name: "App",
  components: {
    vue100vh,
    Header,
    Footer,
  },
};
</script>

<style>
body {
  margin: 0;
  background-image: url("./assets/back-img.png");
  background-size: 60%;
  background-repeat: repeat;
  overflow-x: hidden;
}
#app {
  font-family: "游明朝体", "YuMincho", Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
}
</style>
