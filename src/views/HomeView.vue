<template>
  <div class="page" @click="counter.increment()">
    {{ count }}
  </div>
</template>

<script setup>
import { storeToRefs } from 'pinia'
import { useCounterStore } from '@/store/counter'

const counter = useCounterStore()
const { count } = storeToRefs(counter)
console.log('hello world')
</script>

<style lang="scss" scoped>
.page {
  position: relative;
  display: flex;
  width: 100px;
  color: #333;
}
</style>
