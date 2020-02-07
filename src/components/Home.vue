<template>
  <div id="home-page" class="home">
    <ImageCarousel />
    <div class="hours">
      <span class="hours-header">SHOP HOURS</span>
      <span class="mon-sat">Monday-Saturday:</span>
      <span class="sunday">Sunday:</span>
      <span class="mon-sat-hours">5am - 2:30pm</span>
      <span class="sunday-hours">6am - 12:30pm</span>
    </div>
  </div>
</template>

<script>
import ImageCarousel from "./ImageCarousel";

export default {
  name: "home",
  components: {
    ImageCarousel
  }
};
</script>

<style>
@font-face {
  font-family: HeaderFont;
  src: url("../fonts/IMFellDoublePica-Regular.ttf");
}
.home {
  width: 100%;
  height: auto;
}

.hours {
  width: 30%;
  height: 4rem;
  margin: 4rem auto;
  text-align: left;
  font-family: sans-serif;
  font-size: 2rem;
  font-weight: normal;
  display: grid;
  grid-template-columns: 1fr 1fr;
  grid-template-rows: 1fr 1fr 1fr;
}

.hours-header {
  text-align: center;
  font-size: 3rem;
  font-weight: normal;
  margin-bottom: 2rem;
  font-family: HeaderFont;
  grid-column-start: 1;
  grid-column-end: 3;
  grid-row-start: 1;
  grid-row-end: 2;
}

.mon-sat {
  grid-column-start: 1;
  grid-column-end: 2;
  grid-row-start: 2;
  grid-row-end: 3;
}

.sunday {
  grid-column-start: 1;
  grid-column-end: 2;
  grid-row-start: 3;
  grid-row-end: 4;
}

.mon-sat-hours {
  grid-column-start: 2;
  grid-column-end: 3;
  grid-row-start: 2;
  grid-row-end: 3;
}

.sunday-hours {
  grid-column-start: 2;
  grid-column-end: 3;
  grid-row-start: 3;
  grid-row-end: 4;
}
</style>
