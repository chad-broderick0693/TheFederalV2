<template>
  <div class="nav-bar">
    <ul>
      <li id="home">Home</li>
      <li id="about">About</li>
      <li id="menu">Menu</li>
    </ul>
  </div>
</template>

<script>
export default {
  name: "navbar"
};
</script>

<style>
ul {
  list-style-type: none;
  font-size: 1.8rem;
  margin-top: 1rem;
}

li {
  display: inline;
  margin: 2.5rem;
  cursor: pointer;
  transition: all 0.3s;
}

li:hover {
  border-bottom: 0.2rem solid grey;
  border-radius: 20%;
}
</style>
