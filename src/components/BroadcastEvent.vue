<template>
  <div class="component">
    <h1>Componente que Emite Evento</h1>
    <p>{{ item }} (R${{ price.toFixed(2).replace(".", ",") }})</p>
    <button @click="add">Adicionar ao carrinho</button>
  </div>
</template>
  
  <script setup>
import { defineProps } from "vue";

const props = defineProps({
  id: String,
  item: String,
  price: Number,
});

const emit = defineEmits(["wasAdded"]);

function add() {
  emit("wasAdded", props.price);
}
</script>