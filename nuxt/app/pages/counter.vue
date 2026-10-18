<script setup>
import { ref } from 'vue';
const count = ref(0);

function increment() {
  count.value++
}
</script>

<template>
  <div>
    <h1>Counter: {{ count }}</h1>
    <button @click="increment">+</button>
  </div>
</template>