<template>
  <div class="w-full rounded m-1 p-3 text-right lead font-weight-bold text-white calculator-display">
    {{ value || 0 }}
  </div>
</template>

<script setup>
import { defineProps } from 'vue';

const props = defineProps({
  value: {
    type: String,
    required: true
  }
});
</script>

<style scoped>
.calculator-display {
  background: #222;
  color: #fff;
  font-size: 2em;
  padding: 0.5em;
  text-align: right;
  background-color: #1A1A1D;
}
</style>