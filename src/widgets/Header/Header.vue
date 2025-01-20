<template>
  <div class="header">
    <div class="inner-wrapper">
      <div class="header__content">
        <div class="header__logo cursor-pointer">
          <img :src="Slides" alt="slides" />
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
    </div>
  </div>
</template>

<script setup lang="ts">
import Slides from '../../entities/images/Slides.svg';
import Btn from '../../features/Buton/Btn.vue';
</script>

<style lang="scss">
.header {
  display: flex;
  position: fixed;
  top: 0;
  right: 0;
  left: 0;
  z-index: 1;
  align-items: center;
  justify-content: space-between;
  height: 70px;
  padding: 8px 0;
  background: #fff;
  box-shadow: 0 1px 1px 0 #00000012;

  .header__content {
    display: flex;
    align-items: center;
    justify-content: space-between;
    width: 100%;

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
