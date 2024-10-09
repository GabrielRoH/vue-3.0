<template>
  <div class="component">
    <h1>Componente com Props</h1>
    <p>{{ item }} (R${{ price.toFixed(2).replace(".", ",") }})</p>
  </div>
</template>

<script setup>
import { defineProps } from "vue";

defineProps({
  id: String,
  item: String,
  price: Number,
});
</script>