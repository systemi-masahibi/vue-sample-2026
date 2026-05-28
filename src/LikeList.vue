<script setup>
import { ref } from 'vue'

const likes = ref([])

const addLike = () => { likes.value.push('👍 いいねしました！') }
</script>

<template>
  <h1>演習4：簡易「いいね！」リスト</h1>
  <div>
    <button @click="addLike">いいね！</button>
    <ul>
      <li v-for="(like, index) in likes" :key="index">{{ like }}</li>
    </ul>
  </div>
</template>
