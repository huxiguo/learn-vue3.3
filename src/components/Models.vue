<script setup lang="ts">
import { watchEffect } from 'vue'

const props = defineProps(['modelValue'])
//    1. 在父组件中使用v-model绑定了一个变量，这个变量会被自动转换为modelValue
//    2. 在子组件中使用props接收了modelValue，这个modelValue是只读的
//    3. 在子组件中使用defineEmits定义了一个事件，这个事件会被自动转换为update:modelValue
//    4. 在子组件中使用emit触发了update:modelValue事件，这个事件会自动更新父组件中的modelValue
const emit = defineEmits(['update:modelValue'])
watchEffect(() => {
  console.log(props.modelValue)
})

function onInput(e: Event) {
  emit('update:modelValue', (e.target as HTMLInputElement)?.value)
}
</script>

<template>
  <input :value="modelValue" @input="onInput" />
</template>
