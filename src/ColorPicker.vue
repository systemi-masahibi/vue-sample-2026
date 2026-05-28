<script setup>
import { ref } from 'vue'

const color = ref('lightgray')
const inputColor = ref('')

const applyInput = () => {
  if (inputColor.value) color.value = inputColor.value
}
</script>

<template>
  <h1>演習5：カラーピッカー ＆ プレビュー</h1>
  <div style="text-align: center">
    <div :style="{ width: '200px', height: '200px', backgroundColor: color, margin: '0 auto' }"></div>
    <div>
      <button @click="color = 'red'">赤</button>
      <button @click="color = 'blue'">青</button>
      <button @click="color = 'green'">緑</button>
    </div>
    <p>現在は {{ color }} が選択されています</p>
    <div>
      <input v-model="inputColor" type="text" placeholder="色名を入力（例: orange）" />
      <button @click="applyInput">適用</button>
    </div>
  </div>
</template>
