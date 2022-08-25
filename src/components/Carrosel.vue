<template>
  <Carousel :autoplay="3000" :wrap-around="true" :itemsToShow="1">
    <Slide v-for="slide in 5" :key="slide">
      <div class="carousel__item"><img src="../assets/img/BemVIndo.png" alt=""></div>
    </Slide>

    <template #addons>
      <Navigation />
      <Pagination />
    </template>
  </Carousel>
</template>

<script>
import { Carousel, Navigation, Pagination, Slide } from "vue3-carousel";

import "vue3-carousel/dist/carousel.css";

export default ({
  name: "CAROUSEL",
  components: {
    Carousel,
    Slide,
    Pagination,
    Navigation,
  },
});
</script>

<style>
.carousel__item {
  min-height: 200px;
  max-width: 900px;
  width: 100%;
  background: linear-gradient(#2645a3, #5089f5);
  background-repeat: no-repeat;
  color: black;
  font-size: 20px;
  border-radius: 8px;
  display: flex;
  justify-content: center;
  align-items: center;
}

.carousel__slide {
  padding: 10px;
}

.carousel__prev,
.carousel__next {
  box-sizing: content-box;
  border: 5px solid white;
}
</style>
