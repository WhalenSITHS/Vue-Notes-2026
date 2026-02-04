<template>
  <div>
    <form action="submit" @submit.prevent="login(user)">
      <label for="username">Username</label>
      <input type="text" v-model="user.username" />
      <label for="password">Password</label>
      <input type="password" v-model="user.password" />
    </form>
  </div>
</template>

<script setup>
//add new ref for loggedIn: Boolean. new function to update that value
import { reactive, ref } from 'vue'
const user = reactive({ username: '', password: '' })
</script>

<style lang="scss" scoped></style>
