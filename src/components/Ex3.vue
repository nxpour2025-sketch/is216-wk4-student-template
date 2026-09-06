<script setup>
import { ref } from 'vue'

// Add code here
const login = ref('username')
</script>

<template>
  <h1>Please select your login option</h1>
  <!-- Add/modify code in the following to have a dropdown list 
        which lets the user to select either to login with username or email -->
  <select name="login" v-model="login">
    <option value="username" selected>Username login</option>
    <option value="email">Email login</option>
  </select>

  <div>
    <template v-if="login == 'username'">
      <label>Username</label>
      <input placeholder="Enter your username" />
    </template>
    <template v-else="login == 'email'">
      <label>Email</label>
      <input placeholder="Enter your email address" />
    </template>
  </div>
</template>
