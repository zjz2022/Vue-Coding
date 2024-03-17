<!-- Child.vue -->
<script setup lang="ts">
import { onMounted, inject, onUnmounted } from "vue"

const timer = inject("timer")
const count = inject("count")

onMounted(() => {
  // 切换子组件时, 定时器将不正常工作, 让我们来修复它 . 
  timer.value = window.setInterval(() => {
    count.value++
  }, 1000)
})
onUnmounted(() => {
  window.clearInterval(timer.value)
  timer.value = null
})

</script>

<template>
  <div>
    <p>
      Child Component: {{ count }}
    </p>
  </div>
</template>