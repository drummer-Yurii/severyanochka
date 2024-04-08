<script setup lang="ts">
import { Carousel, Slide } from 'vue3-carousel'
import { Typography } from '@/shared/typography';
import bg from '@/assets/slide-1-bg.png'

const slides = [
  { background: bg, text: 'Доставка бесплатно от 1000 ₽' },
  { background: bg, text: 'Доставка платно' }
]
</script>

<template>
  <carousel class="carousel" :items-to-show="1" :wrapAround="true" :autoplay="3000">
    <slide v-for="slide in slides" :key="slide.text">
      <div class="slide">
        <img class="slide__background" :src="slide.background" alt="bg" />
        <Typography class="slide__text" tagName="h2" bold>
          {{ slide.text }}
        </Typography>
      </div>
    </slide>
  </carousel>
</template>

<style scoped>
.slide {
  position: relative;
  display: flex;
  justify-content: center;
  align-items: center;
  width: 100%;
  height: 200px;
}

.slide__background {
  position: absolute;
  top: 0;
  left: 0;
  z-index: -1;
  width: 100%;
}

.slide__text {
  margin-left: 20%;
  user-select: none;
}
</style>
