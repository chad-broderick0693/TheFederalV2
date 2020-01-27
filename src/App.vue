<template>
  <div id="app">
    <Header />
    <Home />
    <Footer />
  </div>
</template>

<script>
import Header from "./components/Header";
import Home from "./components/Home";
import Footer from "./components/Footer";

export default {
  name: "app",
  components: {
    Header,
    Home,
    Footer
  }
};
</script>

<style>
*,
*::before,
*::after {
  padding: 0;
  margin: 0;
  box-sizing: border-box;
}

body {
  background-image: url("./assets/parchment-background.jpg");
  font-size: 62.5%;
}

#app {
  height: 100vh;
  width: 100vw;
}
</style>
