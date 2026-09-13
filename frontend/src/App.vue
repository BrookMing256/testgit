<script setup>
import { ref } from 'vue'

const message = ref('正在连接后端...')
const loading = ref(false)

async function checkBackend() {
  loading.value = true
  try {
    const response = await fetch('http://localhost:8080/api/hello')
    if (!response.ok) throw new Error('请求失败')
    const data = await response.json()
    message.value = data.message
  } catch (error) {
    message.value = '暂时无法连接后端，请确认 Spring Boot 已启动。'
  } finally {
    loading.value = false
  }
}
</script>

<template>
  <main class="container">
    <section class="card">
      <p class="eyebrow">GIT + SPRING CLOUD 学习项目</p>
      <h1>前后端项目已经准备好了</h1>
      <p class="intro">这是一个简单的 Vue 前端，可以调用 Spring Boot 后端接口。</p>
      <div class="status">{{ message }}</div>
      <button :disabled="loading" @click="checkBackend">
        {{ loading ? '请求中...' : '测试后端接口' }}
      </button>
    </section>
  </main>
</template>
