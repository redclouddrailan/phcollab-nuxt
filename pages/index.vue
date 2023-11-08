<script setup>
import { Pagination, EffectFade, Mousewheel } from "swiper/modules";
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
    :modules="[Pagination, EffectFade, Mousewheel]"
    :slides-per-view="1"
    :loop="false"
    :autoplay="{
      delay: 8000,
      disableOnInteraction: true,
    }"
    :mousewheel="true"
  >
    <SwiperSlide
      v-for="(slide, idx) in slides"
      :key="idx"
      class="bg-fixed bg-cover bg-[url('assets/images/bg.png')]"
    >
      <component :is="slide.component"></component>
      <footer>
        <div class="icon-container">
          <NuxtLink><Icon name="uil:linkedin" width="30" height="30"/></NuxtLink>
          <NuxtLink><Icon name="uil:facebook" width="30" height="30"/></NuxtLink>
          <NuxtLink><Icon name="uil:twitter" width="30" height="30"/></NuxtLink>
          <NuxtLink><Icon name="uil:instagram" width="30" height="30"/></NuxtLink>
        </div>
        <div class="copy-right">
         
          <p>All rights reserved |  phCollab | 2023</p>
        </div>      
      </footer>
    </SwiperSlide>

    <!-- useSwiper() within a swiper instance -->
    <!-- <SwiperControls /> -->
  </Swiper>
</template>
