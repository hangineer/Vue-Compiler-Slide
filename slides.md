---
# try also 'default' to start simple
theme: 'seriph'
# random image from a curated Unsplash collection by Anthony
# like them? see https://unsplash.com/collections/94734566/slidev
background: https://cover.sli.dev
# some information about your slides (markdown enabled)
title: Vue.js 設計實戰
info: |
  ## Slidev Starter Template
  Presentation slides for developers.

  Learn more at [Sli.dev](https://sli.dev)
# apply UnoCSS classes to the current slide
class: text-center
# https://sli.dev/features/drawing
drawings:
  persist: false
# slide transition: https://sli.dev/guide/animations.html#slide-transitions
transition: slide-left
# enable MDC Syntax: https://sli.dev/features/mdc
mdc: true
# duration of the presentation
duration: 35min
# enable text selection and copy
selectable: true
---
<div class="flex justify-center items-center gap-4 text-green-300">
  <logos-vue class="text-4xl" />
  <h1 class="text-cyan-300">Vue.js 設計實戰</h1>
</div>
<h2>第 15 章 編譯器核心技術概覽</h2>
<p>Date: 2026/02/05</p>
<p>presenter: Hannah</p>

<div class="abs-br m-6 text-xl">
  <a href="https://github.com/HcySunYang/code-for-vue-3-book/tree/master/course6-%E7%BC%96%E8%AF%91%E5%99%A8" target="_blank" class="slidev-icon-btn">
    <carbon:logo-github />
  </a>
</div>

<!--
The last comment block of each slide will be treated as slide notes. It will be visible and editable in Presenter Mode along with the slide. [Read more in the docs](https://sli.dev/guide/syntax.html#notes)
-->


---
transition: fade-out
---



# Outline
探討 Vue.js 如何將模板 DSL 轉換為可在瀏覽器運行的 JS 渲染函式
- **15.1 模板 DSL 的編譯器**
- **15.2 parser 的實作原理與狀態機**
- **15.3 建構 AST**
- **15.4 AST 的轉換與插件化架構**
  - **15.4.1 節點的訪問**
  - **15.4.2 轉換上下文與節點的操作**
  - **15.4.3 進入與退出**
- **15.5 將模板 AST 轉為 JavaScript AST**
- **15.6 程式碼生成**
- **總結**
<br>
<br>

<style>
li {
  font-size: 22px;
}
</style>

---
src: ./pages/15.1.md
---

---
src: ./pages/15.2.md
---

---
src: ./pages/15.3.md
---


---
src: ./pages/15.4.md
---


---
src: ./pages/15.5.md
---

---
src: ./pages/15.6.md
---


---
src: ./pages/conclusion.md
---

---
src: ./pages/quiz.md
---
