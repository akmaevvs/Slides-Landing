<template>
  <div class="first-page">
    <div class="content-left">
      <div class="content-left__title">Static website generator, create websites easily.</div>
      <div class="content-left__content">
        <div class="content-left__description">
          Generate beautiful, animated, static websites with your creative direction in a matter of
          minutes. Yes, minutes.
        </div>
        <div class="content-left__btn">
          <Btn>Open the App</Btn>
          <Btn type="secondary">Pricing</Btn>
        </div>
      </div>
    </div>
    <div class="content-right">
      <div class="content-right__img">
        <img :src="Frame" alt="Frame" />
      </div>
    </div>
  </div>
</template>

<script setup lang="ts">
import Btn from '@/features/Buton/Btn.vue';
import Frame from '@/entities/images/Frame.svg';
</script>
<style lang="scss">
.test {
  display: grid;
}

.first-page {
  display: flex;
  gap: 110px;
}

.content-left {
  display: grid;
  width: 100%;
  height: 343px;
  min-width: 460px;
  gap: 22px;

  &__content {
    display: grid;
    gap: 10px;
  }

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

.content-right {
  position: relative;
}

.content-right__img {
  position: relative;
}

.content-right__img::before {
  content: '';
  position: absolute;
  top: 200px;
  left: -100px;
  width: 200px;
  height: 200px;
  transform: translateY(-50%);
  background-image: url('@/entities/images/Circle.svg');
  background-size: cover;
  background-position: center;
  clip-path: inset(0 50% 0 0);
}

.content-right__img::after {
  content: '';
  position: absolute;
  bottom: 30px;
  right: -20px;
  width: 65px;
  height: 47px;
  background: #2164e1;
  border-radius: 10px;
}
</style>
