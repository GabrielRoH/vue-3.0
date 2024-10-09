<template>
  <div class="component">
    <h1>Componente com dados Reativos Não Primitivos</h1>
    <p>Nome: {{ person.name }} | Idade: {{ person.age }}</p>
    <button @click="person.changeName()">Mudar Nome</button> |
    <button @click="person.haveBirthday()">Fazer Aniversário</button>
  </div>
</template>
    
  <!-- Jeito que a rapasiada usa -->
  <script setup>
import { reactive } from "vue";

const person = reactive({
  name: "Ana",
  age: 27,
  changeName() {
    person.name = "Ana Maria Braga";
  },
  haveBirthday() {
    person.age += 1;
  },
});

// function changeName() {
//   person.name = "Ana Maria Braga";
// }

// function haveBirthday() {
//   person.age += 1;
// }
</script>
    
    
<style scoped>
</style>
    