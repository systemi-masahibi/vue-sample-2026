<script setup>
import { ref } from 'vue'

const text = ref('')
</script>

<template>
  <h1>演習3：リアルタイム・文字数カウンター</h1>
  <div>
    <textarea v-model="text"></textarea>
    <p :style="{ color: text.length > 140 ? 'red' : 'black' }">現在 {{ text.length }} 文字です</p>
  </div>
</template>
