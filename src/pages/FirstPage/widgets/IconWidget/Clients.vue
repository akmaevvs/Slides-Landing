<template>
  <div class="content-icons">
    <img
      v-for="icon in icons"
      :key="icon.name"
      :src="icon.component"
      :alt="icon.name"
      class="icon"
    />
  </div>
</template>

<script setup lang="ts">
import Nike from '@/pages/FirstPage/widgets/IconWidget/images/Nike.svg';
import A from '@/pages/FirstPage/widgets/IconWidget/images/A.svg';
import Image from '@/pages/FirstPage/widgets/IconWidget/images/IMAGE.svg';
import Ikea from '@/pages/FirstPage/widgets/IconWidget/images/Ikea.svg';
import T from '@/pages/FirstPage/widgets/IconWidget/images/T.svg';
import GoDaddy from '@/pages/FirstPage/widgets/IconWidget/images/GoDaddy.svg';
import Disney from '@/pages/FirstPage/widgets/IconWidget/images/Disney.svg';
import Nasa from '@/pages/FirstPage/widgets/IconWidget/images/Nasa.svg';

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
.content-icons {
  display: flex;
  justify-content: space-between;
  gap: 60px;
}
</style>
