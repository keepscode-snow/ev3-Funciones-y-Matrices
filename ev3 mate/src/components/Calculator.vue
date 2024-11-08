<template>
  <div class="calculator">
    <CalculatorDisplay :value="displayValue" />
    <div class="calculator-buttons">
      <CalculatorButton v-for="button in buttons" :key="button" :label="button" @press="handleButtonPress" />
    </div>
  </div>
</template>

<script setup>
import { ref } from 'vue';
import CalculatorDisplay from './CalculatorDisplay.vue';
import CalculatorButton from './CalculatorButton.vue';

const displayValue = ref('0');
const buttons = ['7', '8', '9', '/', '4', '5', '6', '*', '1', '2', '3', '-', '0', '.', '=', '+'];

const handleButtonPress = (label) => {
  if (label === '=') {
    displayValue.value = eval(displayValue.value).toString();
  } else {
    displayValue.value += label;
  }
};
</script>

<style scoped>
.calculator {
  display: flex;
  flex-direction: column;
  align-items: center;
  margin: 2em;
}

.calculator-buttons {
  display: grid;
  grid-template-columns: repeat(4, 1fr);
  gap: 0.5em;
}
</style>