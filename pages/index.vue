<script setup>
import { Pagination, EffectFade, Mousewheel } from "swiper/modules";
import { Feature, Gallery, Home } from "#components";
import "swiper/css/pagination";
import "swiper/css/effect-fade";

const slides = markRaw([
  { id: 1, component: Home },
  { id: 2, component: Feature },
  { id: 3, component: Gallery },
]);
</script>

<template>
  <Swiper
    class="h-screen"
    :direction="'vertical'"
    :pagination="{
      clickable: true,
    }"
    :effect="'fade'"
    :modules="[Pagination, EffectFade, Mousewheel]"
    :slides-per-view="1"
    :loop="false"
    :autoplay="{
      delay: 8000,
      disableOnInteraction: true,
    }"
    :mousewheel="true"
  >
    <SwiperSlide v-for="(slide, idx) in slides" :key="idx">
      <component :is="slide.component" />
      <Footer />
    </SwiperSlide>

    <!-- useSwiper() within a swiper instance -->
    <!-- <SwiperControls /> -->
  </Swiper>
</template>
