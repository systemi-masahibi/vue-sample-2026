<script setup>
import { ref, computed } from 'vue'

const words = ['frontend', 'backend', 'javascript', 'component', 'vue', 'reactive', 'template', 'database']
const currentIndex = ref(0)
const input = ref('')
const practicing = ref(true)

const cleared = computed(() => currentIndex.value >= words.length)

const handleInput = () => {
  if (input.value === words[currentIndex.value]) {
    input.value = ''
    currentIndex.value++
  }
}
</script>

<template>
  <h1>演習6：タイピングゲーム</h1>
  <div>
    <button @click="practicing = !practicing">{{ practicing ? '練習を終える' : '練習を始める' }}</button>
    <hr />
    <div v-if="practicing">
      <p v-if="cleared">🎉 クリア！</p>
      <div v-else>
        <p>お題: <strong>{{ words[currentIndex] }}</strong></p>
        <input v-model="input" @input="handleInput" type="text" placeholder="ここにタイプ！" />
        <p>現在の入力: {{ input }}</p>
      </div>
    </div>
  </div>
</template>
