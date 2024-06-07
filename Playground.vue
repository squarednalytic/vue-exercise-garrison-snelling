<template>
  <div class="playground">
    <h1>VueUse Playground</h1>
    <div class="example">
      <h2>Mouse Position</h2>
      <p>X: {{ x }}</p>
      <p>Y: {{ y }}</p>
    </div>
    <div class="example">
      <h2>Counter</h2>
      <p>Count: {{ count }}</p>
      <button @click="increment">Increment</button>
      <button @click="decrement">Decrement</button>
    </div>
  </div>
</template>

<script setup>
import { useMouse, useCounter } from '@vueuse/core'

const { x, y } = useMouse()
const { count, inc: increment, dec: decrement } = useCounter()
</script>

<style scoped>
.playground {
  padding: 20px;
}
.example {
  margin-bottom: 20px;
}
</style>

