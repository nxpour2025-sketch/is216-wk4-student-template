<script setup>
import { ref } from 'vue'

// Add code here
const me = ref('/assets/me.png')
const width = ref('600')
const height = ref('400')

const obj = {
  src: "../assets/wad.png",
  width: 400,
  height: 400,
}
</script>

<template>
  <!-- Add code here -->
   <!--multiple binding-->
   <img v-bind:src="me" :width="width" :height="height" />
   <hr />
   <!--single binding-->
   <img v-bind="obj" />
</template>
