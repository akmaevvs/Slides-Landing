<template>
  <div class="slides">
    <Header />
    <div class="main">
      <div class="inner-wrapper1 main-content">
        <div class="content-left">
          <div class="content-left__title">Static website generator, create websites easily.</div>
          <div class="content-left__description">
            Generate beautiful, animated, static websites with your creative direction in a matter
            of minutes. Yes, minutes.
          </div>
          <div class="content-left__btn">
            <Btn>Open the App</Btn>
            <Btn type="secondary">Pricing</Btn>
          </div>
        </div>
        <div class="content-right">
          <div class="content-right__img">
            <img :src="Frame" alt="Frame" />
          </div>
        </div>
      </div>
      <div class="content-icons">
        <img
          v-for="icon in icons"
          :key="icon.name"
          :src="icon.component"
          :alt="icon.name"
          class="icon"
        />
      </div>
    </div>
  </div>
</template>

<script setup lang="ts">
import Header from './components/Header.vue';
import Frame from './assets/images/Frame.svg';
import Btn from './components/Btn.vue';
import Nike from './assets/images/Nike.svg';
import A from './assets/images/A.svg';
import Image from './assets/images/IMAGE.svg';
import Ikea from './assets/images/Ikea.svg';
import T from './assets/images/T.svg';
import GoDaddy from './assets/images/GoDaddy.svg';
import Disney from './assets/images/Disney.svg';
import Nasa from './assets/images/Nasa.svg';

const icons = [
  { name: 'Nike', component: Nike },
  { name: 'A', component: A },
  { name: 'Image', component: Image },
  { name: 'Ikea', component: Ikea },
  { name: 'T', component: T },
  { name: 'GoDaddy', component: GoDaddy },
  { name: 'Disney', component: Disney },
  { name: 'Nasa', component: Nasa },
];
</script>

<style lang="scss">
.inner-wrapper {
  display: flex;
  width: 100%;
  padding: 0 130px;
}

.main {
  height: 100dvh;
  padding: 286px 130px 0;
}

.main-content {
  display: flex;
  gap: 110px;
}

.content-left {
  display: grid;
  width: 100%;
  min-width: 460px;
  gap: 22px;

  &__title {
    font-size: 45px;
    font-weight: 400;
    line-height: 56px;
  }

  &__description {
    font-size: 21px;
    line-height: 31px;
  }
}

.content-left__btn {
  display: flex;
  gap: 10px;
}

.content-icons {
  display: flex;
  justify-content: space-between;
  padding-top: 200px;
  gap: 60px;
}
</style>
