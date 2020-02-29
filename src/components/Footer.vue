<template>
  <footer class="footer">
    <div class="footer-content">
      <span class="location">Location:</span>
      <span class="contact">Contact:</span>
      <span class="address">2 W. Main St., Mowrystown OH 45155</span>
      <div class="contact-info">
        <span class="email"
          >Email Address: thefederalcoffeehouse@gmail.com</span
        >
      </div>
    </div>
  </footer>
</template>

<script>
export default {
  name: "footer"
};
</script>

<style>
@font-face {
  font-family: FooterFont;
  src: url("../fonts/IMFellDoublePica-Regular.ttf");
}

.footer {
  display: block;
  width: 100%;
  height: auto;
  margin-top: 7rem;
}

.footer-content {
  margin: auto;
  text-align: center;
  font-family: sans-serif;
  font-size: 2rem;
  font-weight: normal;
  display: grid;
  grid-template-rows: 1fr 3fr;
  grid-template-columns: 1fr 2fr 2fr 1fr;
}

.location {
  font-family: FooterFont;
  font-size: 3rem;
  grid-column-start: 2;
  grid-column-end: 3;
  grid-row-start: 1;
  grid-row-end: 2;
}

.contact {
  font-family: FooterFont;
  font-size: 3rem;
  grid-column-start: 3;
  grid-column-end: 4;
  grid-row-start: 1;
  grid-row-end: 2;
}

.address {
  font-size: 2rem;
  grid-column-start: 2;
  grid-column-end: 3;
  grid-row-start: 2;
  grid-row-end: 3;
  margin-top: 2rem;
}

.contact-info {
  font-size: 2rem;
  grid-column-start: 3;
  grid-column-end: 4;
  grid-row-start: 2;
  grid-row-end: 3;
  margin-top: 2rem;
}
</style>
