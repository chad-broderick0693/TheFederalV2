<template>
  <div id="app">
    <Header id="header" />
    <div class="content-container">
      <Home id="home-page" />
      <Footer id="footer" />
    </div>
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

html {
  height: 100%;
}

body {
  background-image: url("./assets/parchment-background.jpg");
  font-size: 62.5%;
  min-height: 100%;
}

#app {
  min-height: 100vh;
  display: grid;
}

.content-container {
  grid-template-columns: 1fr;
  grid-template-rows: 1fr auto;
}
#footer {
  height: 10rem;
  grid-row-start: 2;
  grid-row-end: 3;
}
</style>
