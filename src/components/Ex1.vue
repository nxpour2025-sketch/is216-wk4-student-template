<script setup>
import { ref } from 'vue'

// Add code here
// challenge: use array
const message = ref('Choose your favourite fruit: ')
const fruits = ['apple', 'orange', 'peach']
const selectedFruit = ref('') 

</script>

<template>
  {{ message }}

  <label v-for="fruit in fruits" :key="fruit"> <input type="radio" name="fruit" :value="fruit" v-model="selectedFruit"/> {{ fruit }} </label>
</template>

<style scoped></style>
