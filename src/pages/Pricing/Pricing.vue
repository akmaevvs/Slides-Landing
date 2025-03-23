<template>
  <div class="pricing-title">Pricing</div>
  <div class="pricing-description">
    <div class="pricing-text">Annual</div>
    <Switch />
    <span class="pricing-text">Monthly</span>
  </div>
  <PricingWidget />
</template>

<script setup lang="ts">
import Switch from '@/shared/Switch.vue';
import PricingWidget from '@/pages/Pricing/widgets/PricingWidget.vue';
</script>

<style lang="scss">
.pricing-title {
  font-weight: 700;
  font-size: 63px;
  line-height: 78.75px;
  letter-spacing: 1.39px;
  text-align: center;
}

.pricing-description {
  display: flex;
  gap: 10px;
  align-items: center;
}

.pricing-text {
  font-weight: 400;
  font-size: 18px;
  line-height: 19.8px;
  letter-spacing: 0%;
  text-align: center;
}
</style>
