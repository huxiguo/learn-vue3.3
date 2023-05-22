<script setup lang="ts">
defineSlots<{
  default?: (props: { msg: string }) => any
  item?: (props: { id: number }) => any
}>()
</script>

<template>
  <div>
    <slot msg="123"></slot>
    <slot name="item" :id="13"></slot>
  </div>
</template>
