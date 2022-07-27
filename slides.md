---
class: 'text-center'
theme: default
---

# Start

---

# Intl.NumberFormat
<style>
  .slidev-code-wrapper {
    width: 90%;
    left: 5%;
  }
</style>


<div class="mx-auto my-16">
```ts {2}
interface Number {
  toLocaleString: (locale?: string | string[], options: Intl.NumberFormatOptions) => string
}
```
</div>

<v-click>

```ts {1|3|5|7|9|11}
(12050).toLocaleString('zh') // "12,050"

(12050.7893).toLocaleString('zh') // "12,050.789"

(12050.7893).toLocaleString('zh', { maximumFractionDigits: 2 }) // "12,050.79"

(3500).toLocaleString('zh', { minimumFractionDigits: 2, maximumFractionDigits:2 }) // "3,500.00"

(680000).toLocaleString('zh', { notation: 'compact' }) // "68万"

(680000).toLocaleString('en', { notation: 'compact' }) // "680K"
```
</v-click>

<!-- 备注内容 -->

---

# 完全隔离 React Portal

> Portal 提供了一种将子节点渲染到存在于父组件以外的 DOM 节点的方案。

<div class="text-center mt-32">

[<logos-stackblitz-icon /> StackBlitz 示例](https://stackblitz.com/edit/react-ts-15v7dn?file=index.tsx)

</div>

---
layout: center

---

# Tailwind CSS

---

<div class="grid grid-cols-2">
  <img class="mt-1/3" src="/wechat-notification.png" alt="wechat notification" />

  <div class="h-[480px] overflow-auto">

```html
<div class="chat-notification">
  <div class="chat-notification-logo-wrapper">
    <img class="chat-notification-logo" src="/img/logo.svg">
  </div>
  <div class="chat-notification-content">
    <h4 class="chat-notification-title">Wechat</h4>
    <p class="chat-notification-message">You have a new message!</p>
  </div>
</div>

<style>
  .chat-notification {
    display: flex;
    max-width: 24rem;
    margin: 0 auto;
    padding: 1.5rem;
    border-radius: 0.5rem;
    background-color: #fff;
    box-shadow: 0 20px 25px -5px rgba(0, 0, 0, 0.1),
      0 10px 10px -5px rgba(0, 0, 0, 0.04);
  }
  .chat-notification-logo-wrapper {
    flex-shrink: 0;
  }
  .chat-notification-logo {
    height: 8rem;
    width: 8rem;
  }
  .chat-notification-content {
    margin-left: 1.5rem;
    padding-top: 0.25rem;
  }
  .chat-notification-title {
    color: #1a202c;
    font-size: 1.25rem;
    line-height: 1.25;
  }
  .chat-notification-message {
    color: #718096;
    font-size: 1rem;
    line-height: 1.5;
  }
</style>

```
  
  </div>

</div>

---
layout: center

---

```html
<div class="p-6 max-w-sm mx-auto bg-white rounded-xl shadow-lg flex items-center space-x-4">
  <div class="shrink-0">
    <img class="h-12 w-12" src="/img/logo.svg">
  </div>
  <div>
    <div class="text-xl font-medium text-black">ChitChat</div>
    <p class="text-slate-500">You have a new message!</p>
  </div>
</div>
```

---

## 为什么不直接使用 inline-style ?

- 响应式样式
- 伪类、伪元素
- 设计的一致性
- 样式优先级

## 其他特性

- CSS 文件的大小不会无限增长
- 易用的编辑器插件
- 通过 PostCSS 搭配 Webpack、Rollup、Vite 构建工具使用
- 通过 `@apply` 和 Less、Sass 一起使用

---
layout: center

---
# End
