<template>
  <div class="slides">
    <Header />
    <div class="main">
      <FirstPage />
    </div>
    <ProjectPage />
  </div>
</template>

<script setup lang="ts">
import Header from '@/pages/FirstPage/widgets/Header/Header.vue';
import FirstPage from '@/pages/FirstPage/FirstPage.vue';
import ProjectPage from '@/pages/ProjectPage/ProjectPage.vue';
</script>

<style lang="scss">
.inner-wrapper {
  display: flex;
  width: 100%;
  padding: 0 130px;
}

.slides {
  display: flex;
  flex-direction: column;
  align-items: center;
  min-height: 100vh;
}

.main {
  max-width: 1180px;
  width: 100%;
  flex: 1;
  display: flex;
  justify-content: center;
  align-items: center;
}
</style>
