<template>
  <div class="container">
    <h1>Cookie Clicker</h1>
    <h2>{{ count }}</h2>
    <img @click="increment" src="/cookie.png" alt="" />
  </div>
</template>

<script setup>
import { ref } from 'vue'

const count = ref(0)
function increment() {
  count.value++
}
</script>

<style scoped>
img {
  width: 200px;
  height: auto;
  display: block;
  margin-top: 20px;
}
.container {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  height: 40vh;
}
</style>
