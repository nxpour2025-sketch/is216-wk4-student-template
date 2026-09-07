<script setup>
import { ref } from 'vue'

// Add code here
const me = ref('/assets/me.png');
const width = ref('200');
const height = ref('200');

import wad from '/assets/wad.png'
const obj = {
  src: wad,
  width: 200,
  height: 200,
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
