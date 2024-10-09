<template>
  <div class="component">
    <h1>Componente que Escuta Evento</h1>
    <p>Total: R${{ total }}</p>
    <div class="list">
      <BroadcastEvent item="Item1" :price="1.99" @wasAdded="updateTotal" />
      <BroadcastEvent item="Item2" :price="5.0" @wasAdded="updateTotal" />
      <BroadcastEvent item="Item3" :price="10.99" @wasAdded="updateTotal" />
    </div>
  </div>
</template>

<script setup>
import { ref } from "vue";
import BroadcastEvent from "./BroadcastEvent.vue";

function toFloat(value) {
  return parseFloat(value);
}

const total = ref(0);

function updateTotal(price) {
  const valor = toFloat(total.value) + toFloat(price);
  total.value = valor.toFixed(2);
}
</script>

<style scoped>
.list {
  display: flex;
  justify-content: space-between;
}
</style>