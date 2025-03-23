<template>
  <div class="pricing-container">
    <PricingCard
      title="Free"
      :price="0"
      billedAnnually="No credit card needed."
      :features="[
        { text: 'Limited Slides', available: false },
        { text: 'Limited Settings', available: false },
        { text: 'Limited Effects', available: false },
        { text: 'No Support', available: false },
        { text: 'No Credit Card needed', available: true },
      ]"
    >
      <template #button>
        <Btn>Try for Free</Btn>
      </template>
    </PricingCard>

    <PricingCard
      title="Business"
      :price="21"
      perMonth
      billedAnnually="$249 billed annually. Save $99."
      :features="[
        { text: '20 Exports per Month', available: true },
        { text: 'Unlimited Projects', available: true },
        { text: 'Unlimited Pages', available: true },
        { text: 'Project Management', available: true },
        { text: 'Support and Updates', available: true },
      ]"
    >
      <template #button>
        <Btn type="secondary">Add to Cart</Btn>
      </template>
    </PricingCard>

    <PricingCard
      title="Agency"
      :price="29"
      perMonth
      billedAnnually="$349 billed annually. Save $119."
      :features="[
        { text: 'Unlimited Exports', available: true },
        { text: 'Unlimited Projects', available: true },
        { text: 'Unlimited Pages', available: true },
        { text: 'Project Management', available: true },
        { text: 'Support and Updates', available: true },
      ]"
    >
      <template #button>
        <Btn type="secondary">Add to Cart</Btn>
      </template>
    </PricingCard>
  </div>
</template>

<script setup lang="ts">
import PricingCard from '@/pages/Pricing/widgets/shared/PricingCard.vue';
import Btn from '@/shared/Button/Btn.vue';
</script>

<style lang="scss">
.pricing-container {
  display: flex;
  gap: 20px;
  justify-content: center;
  margin-bottom: 100px;
}
</style>
