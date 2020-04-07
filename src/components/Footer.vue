<template>
  <footer class="footer">
    <div class="footer-content">
      <span class="location">Location</span>
      <span class="contact">Contact</span>
      <span class="social-media">Follow Us</span>
      <div class="social-media-link-container">
        <div class="facebook">
          <a href="https://www.facebook.com/thefederalcoffee/" target="_blank"
            ><img src="../assets/facebook_icon.png"
          /></a>
        </div>
        <div class="instagram">
          <a
            href="https://www.instagram.com/thefederalcoffeehouse/"
            target="_blank"
            ><img src="../assets/instagram_icon.png"
          /></a>
        </div>
      </div>
      <span class="address"
        ><a
          href="https://www.google.com/maps/place/2+W+Main+St,+Mowrystown,+OH+45155/@39.0383328,-83.7509451,17z/data=!3m1!4b1!4m5!3m4!1s0x88412f71ce6dcbef:0x67e963b4bcb461de!8m2!3d39.0383328!4d-83.7487564"
          target="_blank"
          >2 W. Main St., Mowrystown OH 45155</a
        ></span
      >
      <div class="contact-info">
        <span class="phone-number"
          ><a href="tel:9374221777">(937) 422-1777</a></span
        >
        <span class="email">
          <a
            href="https://mail.google.com/mail/?view=cm&fs=1&tf=1&to=thefederalcoffeehouse@gmail.com"
            target="_blank"
            >thefederalcoffeehouse@gmail.com</a
          ></span
        >
      </div>
    </div>
  </footer>
</template>

<script>
export default {
  name: "footer",
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
  grid-template-columns: 1fr 2fr 2fr 2fr 1fr;
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

.social-media {
  font-family: FooterFont;
  font-size: 3rem;
  grid-column-start: 4;
  grid-column-end: 5;
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
  text-align: center;
  font-size: 2rem;
  grid-column-start: 3;
  grid-column-end: 4;
  grid-row-start: 2;
  grid-row-end: 3;
}

.contact-info > span {
  display: block;
  margin-left: 1rem;
  margin-top: 2rem;
}

.social-media-link-container {
  text-align: center;
  font-size: 2rem;
  grid-column-start: 4;
  grid-column-end: 5;
  grid-row-start: 2;
  grid-row-end: 3;
  margin-top: 2rem;
}

.facebook,
.instagram {
  display: inline;
  margin: 3rem;
}

.facebook > a > img,
.instagram > a > img {
  height: 5rem;
  width: 5rem;
}

@media only screen and (max-width: 700px) {
  .footer-content {
    margin: auto;
    text-align: center;
    font-family: sans-serif;
    font-size: 2rem;
    font-weight: normal;
    display: grid;
    grid-template-rows: auto auto auto auto auto auto;
    grid-template-columns: auto;
    grid-row-gap: 2rem;
  }

  .footer-content > * {
    grid-column-start: 1;
    grid-column-end: 2;
  }

  .social-media {
    font-family: FooterFont;
    font-size: 3rem;
    grid-row-start: 1;
    grid-row-end: 2;
  }

  .social-media-link-container {
    text-align: center;
    font-size: 2rem;
    grid-row-start: 2;
    grid-row-end: 3;
  }

  .facebook,
  .instagram {
    display: inline;
    margin: 3rem;
  }

  .location {
    font-family: FooterFont;
    font-size: 3rem;
    grid-row-start: 3;
    grid-row-end: 4;
  }

  .address {
    font-size: 1.8rem;
    grid-row-start: 4;
    grid-row-end: 5;
    margin-top: 0px;
  }

  .contact {
    font-family: FooterFont;
    font-size: 3rem;
    grid-row-start: 5;
    grid-row-end: 6;
  }

  .contact-info {
    text-align: center;
    font-size: 1.8rem;
    grid-row-start: 6;
    grid-row-end: 7;
    margin-bottom: 2rem;
  }

  .contact-info > span {
    margin-left: 0px;
  }

  .phone-number {
    margin-top: 0px !important;
  }
}
</style>
