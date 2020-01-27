<template>
  <div class="header">
    <img class="logo" src="../assets/Logo.svg" alt="the-federal" />
    <NavBar />
  </div>
</template>

<script>
import NavBar from "./NavBar";

export default {
  name: "header",
  components: {
    NavBar
  }
};
</script>

<style>
.header {
  text-align: center;
}

.logo {
  height: 10rem;
  margin: auto;
  margin-top: 1.5rem;
}
</style>
