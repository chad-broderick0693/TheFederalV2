<template>
  <div class="home">
    <ImageCarousel />
    <div class="hours">
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
.home {
  width: 100%;
  height: auto;
}

.hours {
  width: 30%;
  height: 4rem;
  margin: 2rem auto;
  text-align: center;
  font-family: sans-serif;
  font-size: 1rem;
  font-weight: bold;
  display: grid;
  grid-template-columns: 1fr 1fr;
  grid-template-rows: 1fr 1fr;
}

.mon-sat {
  grid-column-start: 1;
  grid-column-end: 2;
  grid-row-start: 1;
  grid-row-end: 2;
}

.sunday {
  grid-column-start: 1;
  grid-column-end: 2;
  grid-row-start: 2;
  grid-row-end: 3;
}

.mon-sat-hours {
  grid-column-start: 2;
  grid-column-end: 3;
  grid-row-start: 1;
  grid-row-end: 2;
}

.sunday-hours {
  grid-column-start: 2;
  grid-column-end: 3;
  grid-row-start: 2;
  grid-row-end: 3;
}
</style>
