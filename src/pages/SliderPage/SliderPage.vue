<template>
  <div class="project-subtitle">
    <img class="cursor-pointer" :src="left" alt="left" />
    <img :src="SliderImage" alt="SliderImage" />
    <img class="cursor-pointer" :src="right" alt="right" />
  </div>
</template>

<script setup lang="ts">
import left from '@/app/assets/images/left.svg';
import right from '@/app/assets/images/right.svg';
import SliderImage from '@/app/assets/images/Slider.svg';

// const images = [SliderImage];
</script>

<style lang="scss"></style>
