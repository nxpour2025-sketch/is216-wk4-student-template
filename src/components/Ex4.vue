<script setup>
import { ref } from 'vue'

// Add code here
// part 1
const id = ref('demo')
const blueBox = ref(true)
const blueBtn = ref(true)
const redBox = ref(false)
const redBtn1 = ref(false)

// part 2
const activeColor = ref('red')
const redBtn = ref(true)
const blueBtn2 = ref(true)

// implement methods below
// part 1
function changeColor() {
  if (blueBox.value) {
    blueBox.value = false
    blueBtn.value = false
    redBox.value = true
    redBtn1.value = true
  } else {
    blueBox.value = true
    blueBtn.value = true
    redBox.value = false
    redBtn1.value = false
  }
}

// part 2
function changeTextColor() {
  if (activeColor.value == 'blue') {
    activeColor.value = 'red'
    redBtn.value = true
    blueBtn2.value = false
  } else {
    activeColor.value = 'blue'
    redBtn.value = false
    blueBtn2.value = true
  }
}
</script>

<template>
  <!-- Add/Modify code here -->
  <!-- note: need to use single quotes '' for classes such as btn-primary which contains '-' signs
                because '-' is a minus operator for (Vue) JavaScript  -->
  <div id="part1">
    <div v-bind:class="{blueBox, redBox}">div ID : {{ id }}</div>

    <button type="button" v-on:click="changeColor" v-bind:class="{'btn-primary': blueBtn, 'btn-danger': redBtn1}">Change Color</button>
  </div>

  <div id="part2">
    <div v-bind:style="{color: activeColor}">div ID : {{ id }}</div>

    <button type="button" v-on:click="changeTextColor" v-bind:class="{'btn-primary': blueBtn2, 'btn-danger': redBtn}">Change Text Color</button>
  </div>
</template>

<style scoped>
.redBox {
  background-color: red;
}
.blueBox {
  background-color: blue;
}
.btn-primary {
  background-color: blue;
  color: white;
}
.btn-danger {
  background-color: red;
  color: white;
}
#demo {
  color: white;
}
</style>
