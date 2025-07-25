<script setup lang="ts">
import HelloWorld from './components/HelloWorld.vue'
import { ref } from 'vue'

const input = ref('')
const loading = ref(false)

const handleClick = () => {
  loading.value = true
  setTimeout(() => {
    loading.value = false
  }, 2000)
}
</script>

<template>
  <div class="app-container">
    <div class="header">
      <a href="https://vite.dev" target="_blank">
        <img src="/vite.svg" class="logo" alt="Vite logo" />
      </a>
      <a href="https://vuejs.org/" target="_blank">
        <img src="./assets/vue.svg" class="logo vue" alt="Vue logo" />
      </a>
      <a href="https://element-plus.org/" target="_blank">
        <img src="https://element-plus.org/images/element-plus-logo-small.svg" class="logo element" alt="Element Plus logo" />
      </a>
    </div>

    <HelloWorld msg="Vite + Vue + Element Plus" />

    <div class="element-demo">
      <h2>Element Plus 组件演示</h2>
      
      <el-space direction="vertical" size="large" style="width: 100%">
        <el-card class="demo-card">
          <h3>按钮演示</h3>
          <el-space>
            <el-button type="primary" :loading="loading" @click="handleClick">
              <el-icon><Search /></el-icon>
              主要按钮
            </el-button>
            <el-button type="success">成功按钮</el-button>
            <el-button type="warning">警告按钮</el-button>
            <el-button type="danger">危险按钮</el-button>
          </el-space>
        </el-card>

        <el-card class="demo-card">
          <h3>输入框演示</h3>
          <el-input 
            v-model="input" 
            placeholder="请输入内容"
            style="width: 300px"
          >
            <template #prefix>
              <el-icon><User /></el-icon>
            </template>
          </el-input>
          <p v-if="input">输入的内容：{{ input }}</p>
        </el-card>

        <el-card class="demo-card">
          <h3>通知演示</h3>
          <el-button @click="$message.success('这是一条成功消息！')">
            显示成功消息
          </el-button>
        </el-card>
      </el-space>
    </div>
  </div>
</template>

<style scoped>
.app-container {
  padding: 20px;
  max-width: 800px;
  margin: 0 auto;
}

.header {
  display: flex;
  justify-content: center;
  align-items: center;
  margin-bottom: 30px;
}

.logo {
  height: 6em;
  padding: 1.5em;
  will-change: filter;
  transition: filter 300ms;
}

.logo:hover {
  filter: drop-shadow(0 0 2em #646cffaa);
}

.logo.vue:hover {
  filter: drop-shadow(0 0 2em #42b883aa);
}

.logo.element:hover {
  filter: drop-shadow(0 0 2em #409effaa);
}

.element-demo {
  margin-top: 40px;
}

.demo-card {
  margin-bottom: 20px;
}

.demo-card h3 {
  margin-bottom: 15px;
  color: #409eff;
}
</style>
