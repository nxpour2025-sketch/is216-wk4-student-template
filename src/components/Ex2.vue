<script setup>
import { ref } from 'vue'

// Add code here
const me = ref('/assets/me.png')
const x = ref('600')
const y = ref('400')

import wad from "/assets/wad.png"
const obj = {
  src: wad,
  width: 400,
  height: 400,
}
</script>

<template>
  <!-- Add code here -->
   <!--multiple binding-->
   <img v-bind:src="me" :width="x" :height="y" />
   <hr />
   <!--single binding-->
   <img v-bind="obj" />
</template>
