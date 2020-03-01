<template>
  <div id="app">
    <Header
      id="header"
      :selected="isSelected"
      @navLinkClicked="setSelectedPage"
    />
    <div class="content-container">
      <component :is="currentPage" />
      <Footer id="footer" />
    </div>
  </div>
</template>

<script>
import Header from "./components/Header";
import Home from "./components/Home";
import About from "./components/About";
import Menu from "./components/Menu";
import Footer from "./components/Footer";

export default {
  name: "app",
  components: {
    Header,
    Home,
    About,
    Menu,
    Footer
  },
  data() {
    return {
      currentPage: "Home",
      isSelected: false
    };
  },
  methods: {
    setSelectedPage(selectedItem) {
      this.currentPage = selectedItem;
    }
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
  font-size: 62.5%;
  min-height: 100%;
  height: 100%;
}

body {
  background-image: url("./assets/parchment-background.jpg");
}

#app {
  min-height: 100vh;
  max-width: 100vw;
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
