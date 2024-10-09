<template>
  <header>Vue</header>
  <ComputedProperties />
  <ListemEvent />
  <template v-for="product in products" :key="product.name">
    <PropsComponent :item="product.name" :price="product.price" />
  </template>
  <DataBinding />
  <PrimitiveNonReactiveDataComponent />
  <PrimitiveReactiveDataComponent />
  <DataComponent />
  <FirtsComponent />
</template>

<script setup>
import FirtsComponent from "./components/FirtsComponent.vue";
import DataComponent from "./components/DataComponent.vue";
import PrimitiveReactiveDataComponent from "./components/PrimitiveReactiveDataComponent.vue";
import PrimitiveNonReactiveDataComponent from "./components/PrimitiveNonReactiveDataComponent.vue";
import DataBinding from "./components/DataBinding.vue";
import PropsComponent from "./components/PropsComponent.vue";
import ListemEvent from "./components/ListemEvent.vue";
import ComputedProperties from "./components/ComputedProperties.vue";

const products = [
  { id: "#023", name: "Desktop Gamer", price: 11783 },
  { id: "#046", name: "Tablet S6 MINI", price: 1799 },
  { id: "#092", name: "Mesa Digitalizadora", price: 246.94 },
];
</script>

<style scoped>
</style>
