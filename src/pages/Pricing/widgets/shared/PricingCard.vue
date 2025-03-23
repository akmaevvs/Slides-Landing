<template>
  <div class="pricing-card">
    <h3 class="title">{{ title }}</h3>
    <ul class="features">
      <li v-for="feature in features" :key="feature.text">
        <span :class="feature.available ? 'check' : 'cross'">
          {{ feature.text }}
        </span>
      </li>
    </ul>
    <div class="price">
      <span class="amount">${{ price }}</span>
      <span v-if="perMonth"> / per month</span>
    </div>
    <p v-if="billedAnnually" class="billed-annually">
      {{ billedAnnually }}
    </p>
    <slot name="button"></slot>
  </div>
</template>

<script setup lang="ts">
defineProps<{
  title: string;
  price: number;
  perMonth?: boolean;
  billedAnnually?: string;
  features: { text: string; available: boolean }[];
}>();
</script>

<style lang="scss">
.pricing-card {
  border-radius: 8px;
  padding: 20px;
  text-align: center;
  border: 1px solid #ddd;
  background: #fff;
}

.title {
  font-size: 1.2rem;
  font-weight: bold;
  margin-bottom: 10px;
}

.features {
  list-style: none;
  padding: 0;
  margin: 10px 0;
}

.features li {
  margin-bottom: 6px;
}

.check {
  color: green;
}

.cross {
  color: gray;
}

.price {
  font-size: 1.5rem;
  font-weight: bold;
  margin: 10px 0;
}

.billed-annually {
  font-size: 0.9rem;
  color: gray;
}
</style>
