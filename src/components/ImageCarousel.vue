<template>
  <div class="image-carousel">
    <div class="mySlides fade">
      <img src="../assets/coffee-shop-img1.jpg" />
    </div>

    <div class="mySlides fade">
      <img src="../assets/coffee-shop-img2.jpg" />
    </div>

    <div class="mySlides fade">
      <img src="../assets/coffee-shop-img3.jpg" />
    </div>

    <!-- Next and previous buttons -->
    <a class="prev" @click="plusSlides(-1)">&#10094;</a>
    <a class="next" @click="plusSlides(1)">&#10095;</a>
  </div>
</template>

<script>
export default {
  name: "ImageCarousel",
  data() {
    return {
      slideIndex: 1
    };
  },
  methods: {
    plusSlides(n) {
      this.showSlides((this.slideIndex += n));
    },
    currentSlide(n) {
      this.showSlides((this.slideIndex = n));
    },
    showSlides(n) {
      var i;
      var slides = document.getElementsByClassName("mySlides");
      //var dots = document.getElementsByClassName("dot");
      if (n > slides.length) {
        this.slideIndex = 1;
      }
      if (n < 1) {
        this.slideIndex = slides.length;
      }
      for (i = 0; i < slides.length; i++) {
        slides[i].style.display = "none";
      }
      // for (i = 0; i < dots.length; i++) {
      //   dots[i].className = dots[i].className.replace(" active", "");
      // }
      slides[this.slideIndex - 1].style.display = "block";
      //dots[this.slideIndex - 1].className += " active";
    }
  },
  mounted() {
    this.showSlides(this.slideIndex);
  }
};
</script>

<style>
/* Slideshow container */
.image-carousel {
  max-width: 100rem;
  position: relative;
  margin: auto;
  margin-bottom: 3rem;
}

/* Hide the images by default */
.mySlides {
  display: none;
  border: 2px solid black;
}

img {
  width: 100%;
  height: 100%;
  margin-bottom: -2px;
}

/* Next & previous buttons */
.prev,
.next {
  cursor: pointer;
  position: absolute;
  top: 50%;
  transform: translateY(-50%);
  width: auto;
  padding: 1.6rem;
  color: white;
  font-weight: bold;
  font-size: 7rem;
  transition: 0.6s ease;
  border-radius: 0 3px 3px 0;
  user-select: none;
}

/* Position the "next button" to the right */
.next {
  right: 0;
  border-radius: 3px 0 0 3px;
}

/* Caption text */
.text {
  color: #f2f2f2;
  font-size: 15px;
  padding: 8px 12px;
  position: absolute;
  bottom: 8px;
  width: 100%;
  text-align: center;
}

/* Fading animation */
.fade {
  -webkit-animation-name: fade;
  -webkit-animation-duration: 1.5s;
  animation-name: fade;
  animation-duration: 1.5s;
}

@-webkit-keyframes fade {
  from {
    opacity: 0.4;
  }
  to {
    opacity: 1;
  }
}

@keyframes fade {
  from {
    opacity: 0.4;
  }
  to {
    opacity: 1;
  }
}
</style>
