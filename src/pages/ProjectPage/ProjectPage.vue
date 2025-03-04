<template>
  <div class="wrapper">
    <div class="test">Projects</div>
    <img class="img" :src="New" alt="new" />
  </div>
  <div class="test2">
    Create and edit pages online. Export as finished, ready-to-upload project.
  </div>
</template>
<script setup lang="ts">
import New from '@/app/assets/images/new.svg';
</script>

<style scoped lang="scss">
* {
  background: #241e38;
}

.wrapper {
  position: relative;
  display: inline-block;
}

.test {
  color: white;
  font-weight: 400;
  font-size: 20px;
  line-height: 31.5px;
  text-align: center;
}

.img {
  position: absolute;
  top: -10px;
  right: -40px;
  width: 42px;
  height: 21px;
}

.test2 {
  color: white;
  font-weight: 700;
  font-size: 45px;
  line-height: 56.25px;
  text-align: center;
}
</style>
