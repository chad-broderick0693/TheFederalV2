<template>
  <div class="header">
    <img class="logo" src="../assets/Logo.svg" alt="the-federal" />
    <NavBar :isSelected="isSelected" @nav-clicked="navClicked" />
  </div>
</template>

<script>
import NavBar from "./NavBar";

export default {
  name: "header",
  components: {
    NavBar
  },
  props: {
    isSelected: Boolean
  },
  data() {
    return {
      navLink: ""
    };
  },
  methods: {
    navClicked(selectedItem) {
      this.$emit("navLinkClicked", selectedItem);
    }
  }
};
</script>

<style>
.header {
  text-align: center;
}

.logo {
  height: 15rem;
  margin: auto;
  margin-top: 3.5rem;
  margin-bottom: 2rem;
}

@media only screen and (max-width: 700px) {
  .logo {
    height: 13rem;
  }
}
</style>
