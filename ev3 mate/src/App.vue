<script setup>

import Calculator from './components/Calculator.vue';
</script>

<template>
  <h1 class="title">Numo</h1>
  <div>
    <Calculator />
  </div>
</template>

<style scoped>
.logo {
  height: 6em;
  padding: 1.5em;
  will-change: filter;
  transition: filter 300ms;
}
.logo:hover {
  filter: drop-shadow(0 0 2em #646cffaa);
}
.logo.vue:hover {
  filter: drop-shadow(0 0 2em #42b883aa);
}
.title {
  font-size: 5em;
  margin: 1em;
}
/* Puedes agregar estilos adicionales aquí si es necesario */
</style>
