<!-- Teleport组件 
  <Teleport> 是一个内置组件，它可以将一个组件内部的一部分模板“传送”到该组件的 DOM 结构外层的位置去。
  https://cn.vuejs.org/guide/built-ins/teleport.html -->

<!-- Vue.js提供了一个内置组件，将其插槽内容渲染到另一个DOM，成为该DOM的一部分。

你知道它是什么吗 ? 让我们试试👇: -->
<script setup>

const msg = "Hello World"

</script>

<template>
  <!-- Renders it to a child element of the `body` -->
  <Teleport to="body">
    <span>{{ msg }}</span>
  </Teleport>
</template>