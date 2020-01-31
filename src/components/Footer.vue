<template>
  <footer class="footer">
    <div class="footer-content">
      <span class="location">Location Information</span>
      <span class="contact">Contact Information</span>
    </div>
  </footer>
</template>

<script>
export default {
  name: "footer"
};
</script>

<style>
.footer {
  display: block;
  width: 100%;
  height: auto;
}

.footer-content {
  margin: auto;
  text-align: center;
  font-family: sans-serif;
  font-size: 1rem;
  font-weight: bold;
  display: grid;
  grid-template-rows: 4fr 1fr 4fr;
  grid-template-columns: 1fr 2fr 2fr 1fr;
}

.location {
  grid-column-start: 2;
  grid-column-end: 3;
  grid-row-start: 2;
  grid-row-end: 3;
}

.contact {
  grid-column-start: 3;
  grid-column-end: 4;
  grid-row-start: 2;
  grid-row-end: 3;
}
</style>
