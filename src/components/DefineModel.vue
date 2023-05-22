<script setup lang="ts">
import { ref } from 'vue'
const count = ref(0)
console.log('count', count)
const modelValue = defineModel()
</script>

<template>
  <input v-model="modelValue" />
</template>
