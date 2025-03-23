<template>
  <header class="header">
    <div class="inner-wrapper">
      <div class="header__content">
        <img :src="Slides" alt="slides" class="cursor-pointer" />
        <div class="header__nav">
          <div class="header__nav-items">
            <a href="#">Pricing</a>
            <a href="#">Help</a>
            <a href="#">Login</a>
          </div>
          <Btn>Demo</Btn>
        </div>
      </div>
    </div>
  </header>
</template>

<script setup lang="ts">
import Slides from '@/app/assets/images/Slides.svg';
import Btn from '@/shared/Button/Btn.vue';
</script>

<style lang="scss">
.header {
  display: flex;
  position: sticky;
  width: 100%;
  z-index: 1;
  align-items: center;
  height: 70px;
  background: #fff;
  box-shadow: 0 1px 1px 0 #00000012;

  .header__content {
    display: flex;
    align-items: center;
    justify-content: space-between;
    width: 100%;
    max-width: 1180px;
    margin: 0 auto;

    .header__nav {
      display: flex;
      align-items: center;
      gap: 20px;

      .header__nav-items {
        display: flex;
        gap: 20px;

        a {
          color: #202020;
          text-decoration: none;
        }
      }
    }
  }
}
</style>
