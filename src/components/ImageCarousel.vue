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
      if (n > slides.length) {
        this.slideIndex = 1;
      }
      if (n < 1) {
        this.slideIndex = slides.length;
      }
      for (i = 0; i < slides.length; i++) {
        slides[i].style.display = "none";
      }
      slides[this.slideIndex - 1].style.display = "block";
    }
  },
  mounted() {
    this.showSlides(this.slideIndex);
  }
};
</script>

<style>
.image-carousel {
  max-width: 100rem;
  position: relative;
  margin: auto;
  margin-bottom: 3rem;
}

.mySlides {
  display: none;
  border: 2px solid black;
}

img {
  width: 100%;
  height: 100%;
  height: 55rem;
  margin-bottom: -2px;
}

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

@media only screen and (max-width: 700px) {
  img {
    height: 25rem;
  }
}
</style>
