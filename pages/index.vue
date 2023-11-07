<script setup>
import { Pagination, EffectFade } from "swiper/modules";
import { Feature, Gallery, Home } from "#components";
import "swiper/css/pagination";
import "swiper/css/effect-fade";

const slides = ref([
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
    :modules="[Pagination, EffectFade]"
    :slides-per-view="1"
    :loop="true"
    :autoplay="{
      delay: 8000,
      disableOnInteraction: true,
    }"
  >
    <SwiperSlide
      v-for="(slide, idx) in slides"
      :key="idx"
      class="bg-fixed bg-cover bg-[url('assets/images/bg.png')]"
    >
      <component :is="slide.component"> </component>
    </SwiperSlide>

    <!-- useSwiper() within a swiper instance -->
    <!-- <SwiperControls /> -->
  </Swiper>
</template>
