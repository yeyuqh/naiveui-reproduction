<script setup>
import { ref } from 'vue'
import Cascader from './components/Cascader.vue'

const value = ref(null)
const show = ref(true)
</script>

<template>
  <div id="app">
    <button @click="show = !show">显示 / 隐藏</button>
    <div style="width: 200px; height: 34px;">
      <Cascader v-if="show" v-model="value" />
    </div>
  </div>
</template>

<style>
#app {
  display: flex;
  justify-content: center;
  align-items: center;
  flex-direction: column;
  gap: 12px;
  width: 100vw;
  height: 100vh;
}
</style>
