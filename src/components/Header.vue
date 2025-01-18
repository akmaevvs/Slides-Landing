<template>
  <div class="header">
    <div class="header__logo">
      <img :src="Slides" alt="slides">
    </div>
    <div class="header__nav">
      <div class="header__nav-items">
        <a href="#">Pricing</a>
        <a href="#">Help</a>
        <a href="#">Login</a>
      </div>
      <Btn>Demo</Btn>
    </div>
  </div>
</template>

<script setup lang="ts">
import Slides from '../assets/images/Slides.svg'
import Btn from './Btn.vue'
</script>

<style lang="scss">
.header {
  position: fixed;
  display: flex;
  align-items: center;
  top: 0;
  right: 0;
  left: 0;
  z-index: 1;
  height: 70px;
  padding: 8px 0;
  background: #fff;
  box-shadow: 0px 1px 1px 0px #00000012;

  .header__nav {
    display: flex;
    align-items: center;
    gap: 4px;

    .header__nav-items {
      display: flex;
      gap: 4px;
    }
  }
}
</style>