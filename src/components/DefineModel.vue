<script setup lang="ts">
import { watchEffect } from 'vue'

const modelValue = defineModel()
watchEffect(() => {
  console.log('modelValue', modelValue)
})
</script>

<template>
  <input v-model="modelValue" />
</template>
