<template>
  <div class="component">
    <h1>Componentes com Propriedades Assistidas</h1>
    <p>{{ age }}</p>
    <label>Ano Nascimneto: </label>
    <input type="number" v-model="yearBirth" min="1900" />
    <label>Ano atual: </label>
    <input type="number" v-model="currentYear" min="2000" />
  </div>
</template>
    
  <script setup>
import { computed, ref } from "vue";

const yearBirth = ref(1900);
const currentYear = ref(new Date().getFullYear());
</script>
    
  <style scoped>
label {
  margin: 10px;
}
</style>