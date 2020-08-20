<template>
  <div id="about-page">
    <div class="mission">
      It is the sole aim of the Federal Coffee House to proudly provide its
      community with ethically sourced and locally-roasted coffee, as well as a
      public space for the community to gather and share.
    </div>
    <div class="mission-description">
      Coffee houses played an important role in the American Revolution and the
      founding of the United States. The Federal Coffee House of Mowrystown,
      Ohio continues this lineage of providing an open space for the public to
      gather and share in one another's interests and day-to-day, all in the
      Federal Era style and decor of the time period. After the Revolutionary
      War, patriots were paid for their service by a limited federal government
      in grants of land scattered through the territory now known as the
      Midwest. Knowing this, the Federal Coffee House proudly serves fresh cups
      of ethically-sourced, locally-roasted coffee to our own and surrounding
      communities in a small portion of those granted lands in southwestern
      Ohio.
    </div>
  </div>
</template>

<script>
export default {
  name: "About",
};
</script>

<style>
@font-face {
  font-family: MissionFont;
  src: url("../fonts/IMFellDoublePica-Regular.ttf");
}
#about-page {
  width: 100%;
  text-align: justify;
  margin-bottom: 17.5rem;
}

.mission {
  width: 53vw;
  height: auto;
  font-family: MissionFont;
  font-size: 3rem;
  margin: auto;
  padding: 0 1rem;
}

.mission-description {
  font-family: sans-serif;
  width: 50vw;
  height: auto;
  font-size: 1.8rem;
  margin: auto;
  margin-top: 3rem;
  line-height: 2.5rem;
  padding: 0 1.5rem;
}

@media only screen and (max-width: 700px) {
  .mission {
    width: 95vw;
  }

  .mission-description {
    width: 95vw;
  }
}
</style>
