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
import Nike from '@/app/assets/images/Nike.svg';
import A from '@/app/assets/images/A.svg';
import Image from '@/app/assets/images/IMAGE.svg';
import Ikea from '@/app/assets/images/Ikea.svg';
import T from '@/app/assets/images/T.svg';
import GoDaddy from '@/app/assets/images/GoDaddy.svg';
import Disney from '@/app/assets/images/Disney.svg';
import Nasa from '@/app/assets/images/Nasa.svg';

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
  padding-top: 200px;
  gap: 60px;
}
</style>
