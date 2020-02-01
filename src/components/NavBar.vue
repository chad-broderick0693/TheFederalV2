<template>
  <div class="nav-bar">
    <ul>
      <li id="home" @click="setHomeSelected()">Home</li>
      <li id="about" @click="setAboutSelected()">About</li>
      <li id="menu" @click="setMenuSelected()">Menu</li>
    </ul>
  </div>
</template>

<script>
export default {
  name: "navbar",
  props: ["isSelected"],
  data() {
    return {
      isListItemSelected: false
    };
  },
  methods: {
    setHomeSelected() {
      let home = document.getElementById("home");
      let about = document.getElementById("about");
      let menu = document.getElementById("menu");

      home.classList.add("selected");
      about.classList.remove("selected");
      menu.classList.remove("selected");
      this.$emit("nav-clicked", "Home");
    },
    setAboutSelected() {
      let home = document.getElementById("home");
      let about = document.getElementById("about");
      let menu = document.getElementById("menu");

      home.classList.remove("selected");
      about.classList.add("selected");
      menu.classList.remove("selected");
      this.$emit("nav-clicked", "About");
    },
    setMenuSelected() {
      let home = document.getElementById("home");
      let about = document.getElementById("about");
      let menu = document.getElementById("menu");

      home.classList.remove("selected");
      about.classList.remove("selected");
      menu.classList.add("selected");
      this.$emit("nav-clicked", "Menu");
    }
  }
};
</script>

<style>
@font-face {
  font-family: NavFont;
  src: url("../fonts/IMFellDoublePica-Regular.ttf");
}

ul {
  list-style-type: none;
  font-size: 1.8rem;
  margin-top: 1rem;
}

li {
  font-family: NavFont;
  display: inline;
  margin: 2.5rem;
  cursor: pointer;
  transition: all 0.3s;
}

li.selected {
  border-bottom: 0.2rem solid grey;
}
</style>
