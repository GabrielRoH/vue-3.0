<template>
  <div class="component">
    <h1>Componente com dados Reativos Primitivos</h1>
    <p>Nome: {{ name }} | Idade: {{ age }}</p>
    <button @click="changeName()">Mudar Nome</button> |
    <button @click="haveBirthday()">Fazer Aniversário</button>
  </div>
</template>
  
<!-- Jeito que a rapasiada usa -->
<script setup>
import { ref } from "vue";

const name = ref("Ana");
const age = ref(27);

function changeName() {
  name.value = "Ana Maria Braga";
}

function haveBirthday() {
  age.value += 1;
}
</script>
  
  
  <style scoped>
</style>
  