<script setup lang="ts">
const emit = defineEmits<{
  foo: [id: number]
  bar: [name: string, ...rest: any[]]
}>()

const handleFoo = () => {
  emit('foo', 12)
}
const handleBar = () => {
  emit('bar', 'baz', 1, 2, 3)
}
</script>

<template>
  <div>
    <button @click="handleFoo">foo</button>
    <button @click="handleBar">bar</button>
  </div>
</template>
