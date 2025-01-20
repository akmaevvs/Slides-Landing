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
import Nike from '@/entities/images/Nike.svg';
import A from '@/entities/images/A.svg';
import Image from '@/entities/images/IMAGE.svg';
import Ikea from '@/entities/images/Ikea.svg';
import T from '@/entities/images/T.svg';
import GoDaddy from '@/entities/images/GoDaddy.svg';
import Disney from '@/entities/images/Disney.svg';
import Nasa from '@/entities/images/Nasa.svg';

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
