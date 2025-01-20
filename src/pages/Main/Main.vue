<template>
  <div class="slides">
    <Header />
    <div class="main">
      <div class="main-content">
        <FirstPage />
      </div>
      <Icons />
    </div>
  </div>
</template>

<script setup lang="ts">
import Header from '@/widgets/Header/Header.vue';
import FirstPage from '@/pages/FirstPage/FirstPage.vue';
import Icons from '@/entities/Icons.vue';
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
</style>
