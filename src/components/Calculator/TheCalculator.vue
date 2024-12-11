<script setup>

import CalculatorWidthMore1000 from "./CalculatorWidthMore1000.vue";
import CalculatorWidthMore660 from "./CalculatorWidthMore660.vue";
import CalculatorWidthMore360 from "./CalculatorWidthMore360.vue";

defineProps({
  width: Number,
})

// function moveLeft(){
//
//   let calculatorBody = document.querySelector('.calculator-body')
//
//   console.log(calculatorBody.clientWidth)
// }

</script>

<template>

  <CalculatorWidthMore1000 v-if="width > 1000"/>

  <CalculatorWidthMore660 v-else-if="width > 660"/>

  <CalculatorWidthMore360 v-else />

</template>

<style scoped lang="scss">



</style>