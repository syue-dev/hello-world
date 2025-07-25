# Vue 3 + TypeScript + Vite + Element Plus 项目

这是一个使用 Vite 构建的现代化 Vue 3 项目，集成了 TypeScript 和 Element Plus 组件库。

## 技术栈

- **Vue 3** - 渐进式 JavaScript 框架
- **TypeScript** - JavaScript 的超集，提供类型安全
- **Vite** - 快速的构建工具
- **Element Plus** - 基于 Vue 3 的组件库

## 项目特性

- ⚡️ Vite 快速热重载
- 🎯 TypeScript 类型支持
- 🎨 Element Plus 现代化 UI 组件
- 📦 按需导入优化
- 🔍 完整的图标库支持

## 开始使用

### 安装依赖

```bash
npm install
```

### 启动开发服务器

```bash
npm run dev
```

### 构建生产版本

```bash
npm run build
```

### 预览生产构建

```bash
npm run preview
```

## 项目结构

```
my-vue-app/
├── src/
│   ├── components/     # Vue 组件
│   ├── assets/        # 静态资源
│   ├── App.vue        # 根组件
│   ├── main.ts        # 应用入口
│   └── style.css      # 全局样式
├── public/            # 公共静态文件
├── index.html         # HTML 模板
├── vite.config.ts     # Vite 配置
└── tsconfig.json      # TypeScript 配置
```

## Element Plus 配置

项目已经完整配置了 Element Plus：

- 全量导入 Element Plus 组件
- 自动导入所有图标组件
- 包含样式文件

在组件中可以直接使用 Element Plus 组件：

```vue
<template>
  <el-button type="primary">主要按钮</el-button>
  <el-input v-model="input" placeholder="请输入">
    <template #prefix>
      <el-icon><User /></el-icon>
    </template>
  </el-input>
</template>
```

## 开发建议

1. 使用 TypeScript 进行开发，享受类型安全的好处
2. 参考 Element Plus 官方文档：https://element-plus.org/
3. 使用 Vue 3 Composition API 编写组件
4. 遵循 Vue 3 最佳实践

## 相关链接

- [Vue 3 官方文档](https://v3.vuejs.org/)
- [Vite 官方文档](https://vite.dev/)
- [Element Plus 官方文档](https://element-plus.org/)
- [TypeScript 官方文档](https://www.typescriptlang.org/)
