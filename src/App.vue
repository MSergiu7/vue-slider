<template>
    <div class="container">
      <h1>Vue.js Carousel</h1>
      <app-carousel></app-carousel>
    </div>
</template>

<script>
import Carousel from './components/Carousel.vue'

export default {
    components: {
        'appCarousel': Carousel
    }
}
</script>

<style lang="scss">
    .container {
      width: 1200px;
      margin: 0 auto;
      text-align: center;
    }

    h1 {
      font-family: Karla, Arial, Helvetica, sans-serif;
      color: #001f3f;
    }

    .carousel {
      position: relative;
    }

    .fa-chevron-left, .fa-chevron-right {
      cursor: pointer;
      font-size: 50px;
      color: #001f3f;
      position: absolute;
      top: 50%;
      transform: translateY(-50%);
      z-index: 9999;
    }

    .fa-chevron-left {
      left: 8%;
    }

    .fa-chevron-right {
      right: 8%;
    }

    .slides {
      height: 426px;
    }

    .slide-img {
      position: absolute;
      transform: translateX(-50%);
    }

    .currentSlide {
      z-index: 999;
    }

    .slides {
      transform-style: preserve-3d;
      perspective: 1000px;
    }

    .right-1, .left-1, .right-2, .left-2, .right-3, .left-3 {
      opacity: 0.3;
      visibility: visible;
      background-size: cover;
      box-sizing: border-box;
      transition: transform 500ms ease 0s, opacity 500ms ease 0s, visibility 500ms ease 0s;
    }

    .right-1 {
      transform: translateX(-50px) translateZ(-400px) rotateY(-35deg);
      z-index: 998;
    }

    .left-1 {
      transform: translateX(-600px) translateZ(-400px) rotateY(35deg);
      z-index: 998;
    }

    .right-2 {
      transform: translateX(100px) translateZ(-500px) rotateY(-35deg);
      z-index: 997;
    }

    .left-2 {
      transform: translateX(-750px) translateZ(-500px) rotateY(35deg);
      z-index: 997;
    }

    .right-3 {
      transform: translateX(200px) translateZ(-500px) rotateY(-35deg);
      z-index: 996;
    }

    .left-3 {
      transform: translateX(-850px) translateZ(-500px) rotateY(35deg);
      z-index: 996;
    }
</style>
