<template>
  <div>
    <form action="submit" @submit.prevent="login(user)">
      <label for="username">Username</label>
      <input type="text" v-model="user.username" />
      <label for="password">password</label>
      <input type="password" v-model="user.password" />
      <button type="submit">Login</button>
    </form>
    <h2 v-if="loggedIn">{{ user.username }}</h2>
    <h2 v-else>Please Login</h2>
  </div>
</template>

<script setup>
//create variable loggedIn = false, create finction login console log user and changed loggedIn to true
import { ref, reactive } from 'vue'
const user = reactive({ username: '', password: '' })
const loggedIn = ref(false)
function login(user) {
  console.log(user)
  loggedIn.value = true
}
</script>

<style lang="scss" scoped></style>
