<template>
  <footer class="footer">
    <div class="footer-content">
      <span class="location">Location:</span>
      <span class="contact">Contact:</span>
      <span class="social-media">Social Media Links:</span>
      <div class="social-media-link-container">
        <div class="facebook">
          <a href="https://www.facebook.com" target="_blank"
            ><img
              src="https://img.icons8.com/ios/50/000000/facebook-circled.png"
          /></a>
        </div>
        <div class="instagram">
          <a href="https://www.instagram.com" target="_blank"
            ><img src="https://img.icons8.com/wired/64/000000/instagram-new.png"
          /></a>
        </div>
      </div>
      <span class="address">2 W. Main St., Mowrystown OH 45155</span>
      <div class="contact-info">
        <span class="phone-number">Phone#: (937) 422-1777</span>
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
}

.facebook > a,
.instagram > a {
  display: inline-block;
  height: 5rem;
  width: 5rem;
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

  .location {
    font-family: FooterFont;
    font-size: 3rem;
    grid-row-start: 3;
    grid-row-end: 4;
  }

  .address {
    font-size: 2rem;
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
    font-size: 2rem;
    grid-row-start: 6;
    grid-row-end: 7;
  }

  .contact-info > span {
    margin-left: 0px;
  }

  .phone-number {
    margin-top: 0px !important;
  }
}
</style>
