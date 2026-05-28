<script setup>
import { ref } from 'vue'

const count = ref(0)

const increment = () => { count.value++ }
const decrement = () => { if (count.value > 0) count.value-- }
const reset = () => { count.value = 0 }
</script>

<template>
  <h1>演習1：カウントアップ ＆ リセット</h1>
  <div>
    <h2>現在の数値: {{ count }}</h2>
    <div>
      <button @click="increment">+1</button>
      <button @click="decrement">-1</button>
      <button @click="reset">Reset</button>
    </div>
  </div>
</template>