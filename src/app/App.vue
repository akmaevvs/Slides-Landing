<template>
  <div class="slides">
    <Header />
    <div class="main">
      <FirstPage />
    </div>
    <ProjectPage />
    <SliderPage />
    <Pricing />
    <Contacts />
    <MainFooter />
  </div>
</template>

<script setup lang="ts">
import Header from '@/widgets/MainHeader/MainHeader.vue';
import FirstPage from '@/pages/FirstPage/FirstPage.vue';
import ProjectPage from '@/pages/ProjectPage/ProjectPage.vue';
import SliderPage from '@/pages/SliderPage/SliderPage.vue';
import Pricing from '@/pages/Pricing/Pricing.vue';
import MainFooter from '@/widgets/MainFooter/MainFooter.vue';
import Contacts from '@/pages/Contacts/Contacts.vue';
</script>

<style lang="scss">
.inner-wrapper {
  display: flex;
  width: 100%;
  padding: 0 130px;
}

.main-wrapper {
  //
}

.slides {
  display: flex;
  flex-direction: column;
  align-items: center;
  min-height: 100vh;
  gap: 50px;
  //margin-bottom: 150px;
}

.main {
  margin-top: 130px;
  max-width: 1180px;
  width: 100%;
  display: flex;
  justify-content: center;
  align-items: center;
}
</style>
