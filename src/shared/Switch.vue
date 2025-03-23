<template>
  <div class="switch" :class="{ 'switch-on': isOn }" @click="toggle">
    <div class="slider"></div>
  </div>
</template>

<script setup lang="ts">
import { ref } from 'vue';

const isOn = ref(false);

const toggle = () => {
  isOn.value = !isOn.value;
};
</script>

<style lang="scss">
.switch {
  width: 50px;
  height: 26px;
  background: #ccc;
  border-radius: 15px;
  position: relative;
  cursor: pointer;
  transition: background 0.3s;
}

.switch-on {
  background: #30b467;
}

.slider {
  width: 22px;
  height: 22px;
  background: #fff;
  border-radius: 50%;
  position: absolute;
  top: 50%;
  left: 2px;
  transform: translateY(-50%);
  transition: left 0.3s;
}

.switch-on .slider {
  left: 26px;
}
</style>
