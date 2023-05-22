<script setup lang="ts" generic="T,U extends string">
defineProps<{
  age: T
  name: U[]
}>()
</script>

<template>
  <div>generic</div>
</template>
