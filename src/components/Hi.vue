<script setup lang="ts">
import { watchEffect } from 'vue'

import type { HiProps } from './hi'
// defineProps<HiProps & { age: number }>()

// eslint-disable-next-line
const { msg } = defineProps<HiProps>()

watchEffect(() => {
  console.log(msg)
})
</script>

<template>
  <div>hi</div>
</template>
