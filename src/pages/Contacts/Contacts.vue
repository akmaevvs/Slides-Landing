<template>
  <div class="contacts">
    <div class="inner-wrapper">
      <div class="contacts__content">
        <div class="contacts__text">
          Made with Slides by
          <img :src="icon" alt="icon" />
          <span class="contacts__text-underline"> Designmodo </span>
        </div>

        <div class="contacts__nav">
          <div class="contacts__nav-items">
            <a href="#">Changelog</a>
            <a href="#">License</a>
            <a href="#">Tutorials</a>
            <a href="#">Help</a>
            <a href="#">Login</a>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script setup lang="ts">
import icon from './images/icon.svg';
</script>

<style lang="scss">
.contacts {
  display: flex;
  position: sticky;
  width: 100%;
  z-index: 1;
  align-items: center;
  height: 70px;
  background: #fff;

  .contacts__content {
    display: flex;
    align-items: center;
    justify-content: space-between;
    width: 100%;
    max-width: 1180px;
    margin: 0 auto;

    .contacts__text {
      display: flex;
      align-items: center;
      gap: 5px;
      font-weight: 700;
      font-size: 15px;
      line-height: 18px;
      letter-spacing: 0%;
      text-align: center;

      .contacts__text-underline {
        text-decoration: underline;
        text-underline-offset: 4px;
      }
    }

    .contacts__nav {
      display: flex;
      align-items: center;
      gap: 20px;

      .contacts__nav-items {
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
