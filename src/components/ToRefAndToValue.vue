<script setup lang="ts">
import { ref, toRef, toValue } from 'vue'
const count = ref(2)

const countToRef = toRef(1)
console.log(countToRef)
// 只读属性
const num = toRef(() => 12)
console.log(num)
</script>

<template>
  <div>toRef ---- toValue</div>
</template>
