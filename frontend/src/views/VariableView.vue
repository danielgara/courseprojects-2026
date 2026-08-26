<script setup lang="ts">
import { ref, watch } from 'vue'

const country = ref('')
let message = ''

watch(country, (newCountry) => {
  if (newCountry === 'colombia') {
    message = '🇨🇴 Elegiste el mejor país!'
  } else {
    message = ''
  }
})
</script>

<template>
  <div>
    <select v-model="country">
      <option value="">Seleccione un país</option>
      <option value="colombia">Colombia</option>
      <option value="mexico">México</option>
      <option value="argentina">Argentina</option>
    </select>

    <p v-if="message">{{ message }}</p>
  </div>
</template>