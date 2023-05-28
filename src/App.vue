<script setup lang="ts">
import { useDark, useToggle } from '@vueuse/core'
// import { ref } from 'vue'
// import Hi from './components/Hi.vue'
// import Generic from './components/Generic.vue'
// import EmiterBefore from './components/EmiterBefore.vue'
// import EmiterAfter from './components/EmiterAfter.vue'
// import Sloter from './components/Sloter.vue'
// import Models from './components/Models.vue'
// import DefineModel from './components/DefineModel.vue'
// import DefineOptions from './components/DefineOptions.vue'
import ToRefAndToValue from './components/ToRefAndToValue.vue'

// const count = ref<number>(1)
// const names = ref<string>('')
// const args = ref<any[]>([])
// const msg = ref('wasd')
// const handleEmiterBeforeFoo = (id: number) => {
//   count.value = id
// }
// const handleEmiterBeforeBar = (name: string, ...rest: any[]) => {
//   names.value = name
//   args.value = rest
// }
// function handleEmiterAfterFoo(id: number) {
//   count.value = id
// }
// function handleEmiterAfterBar(name: string, ...rest: any[]) {
//   names.value = name
//   args.value = rest
// }
// const handleChangeMsg = () => {
//   msg.value += '1'
// }
// const model = ref('123123321')
// const handleBtnClick = () => {
//   model.value += '1'
// }
// const handleInput = (args: any) => {
//   console.log(args)
// }
const isDark = useDark()
const toggleDark = useToggle(isDark)
</script>

<template>
  hello world
  <button @click="toggleDark()">type {{ isDark }}</button>
  <!-- <Hi :msg="msg" @click="handleChangeMsg" /> -->
  <!-- <Generic :age="10" :name="['1', '2', '3']" /> -->
  <!-- count---{{ count }} names---{{ names }} args---{{ args }} -->
  <!-- <EmiterBefore @foo="handleEmiterBeforeFoo" @bar="handleEmiterBeforeBar" /> -->
  <!-- <EmiterAfter @foo="handleEmiterAfterFoo" @bar="handleEmiterAfterBar" /> -->
  <!-- <Sloter>
    <template #default="{ msg }">
      {{ msg }}
    </template>
    <template #item="{ id }">
      {{ id }}
    </template>
  </Sloter> -->
  <!-- <Models :model-value="model" @update:model-value="handleInput" /> -->
  <!-- <DefineModel v-model="model" /> -->
  <!-- <button @click="handleBtnClick">+1</button> -->
  <!-- <DefineOptions /> -->
  <ToRefAndToValue />
</template>
