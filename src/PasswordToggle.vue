<script setup>
import { ref } from 'vue'

const isVisible = ref(false)
</script>

<template>
  <h1>演習2：パスワード表示・非表示切り替え</h1>
  <div>
    <input :type="isVisible ? 'text' : 'password'" />
    <button @click="isVisible = !isVisible">{{ isVisible ? '隠す' : '表示' }}</button>
  </div>
</template>
