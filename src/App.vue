<template>
  <div id="app">
    <Header />
    <Home id="home" />
    <Footer id="footer" />
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
  display: flex;
  flex-direction: column;
}

#home {
  flex: 1 0 auto;
  padding: 2rem;
}

#footer {
  flex-shrink: 0;
  padding: 2rem;
}
</style>
