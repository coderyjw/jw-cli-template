<template>
  <div class="main">
    <h2>main: {{ counterStore.counter }}-{{ counterStore.doubleCounter }}</h2>
    <button @click="changeCounter(counterStore.counter - 1)">-1</button>
    <button @click="changeCounter(counterStore.counter + 1)">+1</button>
  </div>
</template>

<script setup lang="ts">
import useCounterStore from '@/store/counter'

const counterStore = useCounterStore()

function changeCounter(number: number) {
  counterStore.changeCounterAction(number)
}
</script>

<style lang="less" scoped>
.main {
  color: red;
}
</style>
