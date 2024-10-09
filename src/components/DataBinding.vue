<template>
  <div class="component">
    <h1>Componente com Data Binding</h1>
    <input type="text" :value="dataBinding" />
    <p>{{ twoWayDataBinding }}</p>
    <input
      type="text"
      placeholder="escreva a frase aqui! @input"
      @input="(e) => (twoWayDataBinding = e.target.value)"
    />
    <input
      type="text"
      placeholder="escreva a frase aqui! model"
      v-model="twoWayDataBinding"
    />
  </div>
</template>


<script setup>
import { ref } from "vue";

const dataBinding = ref("Vue é muito legal!");
const twoWayDataBinding = ref("Vue é o melhor framework!!!");
</script>