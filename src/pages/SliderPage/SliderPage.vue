<template>
  <div class="project-slider">
    <button @click="prevImage">
      <img class="cursor-pointer" :src="left" alt="left" />
    </button>
    <div class="image-container">
      <img :src="currentImage" alt="SliderImage" />
    </div>
    <button @click="nextImage">
      <img class="cursor-pointer" :src="right" alt="right" />
    </button>
  </div>
  <div class="divider"></div>
</template>

<script setup lang="ts">
import { ref, computed } from 'vue';

import left from '@/app/assets/images/left.svg';
import right from '@/app/assets/images/right.svg';
import SliderImage from '@/app/assets/images/Slider.svg';
import Components from '@/app/assets/images/Components.svg';

const images = [SliderImage, Components];

const currentIndex = ref(0);

const currentImage = computed(() => images[currentIndex.value]);

const prevImage = () => {
  currentIndex.value = (currentIndex.value - 1 + images.length) % images.length;
};

const nextImage = () => {
  currentIndex.value = (currentIndex.value + 1) % images.length;
};
</script>

<style lang="scss">
.project-slider {
  display: flex;
  align-items: center;
  justify-content: center;
  position: relative;
  width: 900px;
  height: 500px;
  overflow: hidden;
}

.image-container {
  display: flex;
  align-items: center;
  justify-content: center;
  width: 100%;
  height: 100%;
  border-radius: 8px;
}

.image-container img {
  max-width: 100%;
  max-height: 100%;
  object-fit: contain;
}

.divider {
  height: 1px;
  background: #ddd;
  margin: 16px 0;
  width: 900px;
}
</style>
