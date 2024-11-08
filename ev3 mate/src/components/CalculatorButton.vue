<template>
  <button @click="handleClick" class="calculator-button">
    {{ label }}
  </button>
</template>

<script setup>
import { defineProps, defineEmits } from 'vue';

const props = defineProps({
  label: {
    type: String,
    required: true
  }
});

const emits = defineEmits(['press']);

const handleClick = () => {
  emits('press', props.label);
};
</script>

<style scoped>
.calculator-button {
  background: #444;
  border: none;
  color: #fff;
  font-size: 1.5em;
  margin: 0.2em;
  padding: 1em;
  width: 3em;
  height: 3em;
}
</style>