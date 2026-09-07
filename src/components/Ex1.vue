<script setup>
import { ref } from 'vue'

// Add code here
// challenge: use array
const message = ref('Choose your favorite fruit: ');
const fruits = ref(['apple', 'orange', 'peach']);

</script>
 
<template>
  {{ message }}

  <!-- 
  <label for=""> < input type="radio" name="fruit"> {{ fruits[0] }} >/label>
  <label for=""> < input type="radio" name="fruit"> {{ fruits[1] }} >/label>
  <label for=""> < input type="radio" name="fruit"> {{ fruits[2] }} >/label>
  -->

  <label v-for="fruit in fruits" v-bind:key="fruit">
    <input type="radio" name="fruit"> {{ fruit }}
  </label>
</template>

<style scoped></style>
