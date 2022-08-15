<template>
  <div class="home">
    <HeaderRstore />
    <!-- Hero Section Begin -->
    <Carousel :autoplay="2000" :wrap-around="true">
      <Slide v-for="slide in 5" :key="slide">
        <div class="carousel__item">{{ slide }}</div>
        
        <section class="hero-section">
          <div class="hero-items owl-carousel">
            <div class="single-hero-items set-bg" data-setbg="img/hero-1.jpg">
              <div class="container">
                <div class="row">
                  <div class="col-lg-5">
                    <span>Bag,kids</span>
                    <h1>Black friday</h1>
                    <p>
                      Lorem ipsum dolor sit amet, consectetur adipisicing elit,
                      sed do eiusmod tempor incididunt ut labore et dolore
                    </p>
                    <a href="#" class="primary-btn">Shop Now</a>
                  </div>
                </div>
              </div>
            </div>
            <div class="single-hero-items set-bg" data-setbg="img/hero-2.jpg">
              <div class="container">
                <div class="row">
                  <div class="col-lg-5">
                    <span>Bag,kids</span>
                    <h1>Black friday</h1>
                    <p>
                      Lorem ipsum dolor sit amet, consectetur adipisicing elit,
                      sed do eiusmod tempor incididunt ut labore et dolore
                    </p>
                    <a href="#" class="primary-btn">Shop Now</a>
                  </div>
                </div>
              </div>
            </div>
          </div>
        </section>
      </Slide>

      <template #addons>
        <Pagination />
      </template>
    </Carousel>

    <!-- Hero Section End -->
  </div>
</template>

<script>
// @ is an alias to /src
// import HelloWorld from '@/components/HelloWorld.vue'
import HeaderRstore from "@/components/HeaderRstore.vue";
import { Carousel, Pagination, Slide } from "vue3-carousel";
import "vue3-carousel/dist/carousel.css";

export default {
  name: "HomeView",
  components: {
    HeaderRstore,
    Carousel,
    Pagination,
    Slide,
  },
};
</script>

<style scoped>
.carousel__slide > .carousel__item {
  transform: scale(1);
  opacity: 0.5;
  transition: 0.5s;
}
.carousel__slide--visible > .carousel__item {
  opacity: 1;
  transform: rotateY(0);
}
.carousel__slide--next > .carousel__item {
  transform: scale(0.9) translate(-10px);
}
.carousel__slide--prev > .carousel__item {
  transform: scale(0.9) translate(10px);
}
.carousel__slide--active > .carousel__item {
  transform: scale(1.1);
}
</style>