<template>
  <div class="component">
    <h1>Componente com dados</h1>
    <p>Nome: {{ nameProduct }} - {{ codeProduct }}</p>
  </div>
</template>

<!-- <script>
//  options API
// export default {
//   data: function () {
//     return {
//       nameProduct: "Caderno",
//       codeProduct: "#0321",
//     };
//   },
// };

//  composition API
export default {
  setup: function () {
    const nameProduct = "Lápis"
    const codeProduct = "#0109"
    return {
        nameProduct,
        codeProduct 
    };
  },
};
</script> -->

<!-- Jeito que a rapasiada usa -->
<script setup>
const nameProduct = "Notebook";
const codeProduct = "#0987";
</script>


<style scoped>
</style>
