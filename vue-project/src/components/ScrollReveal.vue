<template>
  <div ref="target" :class="['reveal-wrapper', { 'is-visible': isVisible }]">
    <slot></slot>
  </div>
</template>

<script setup lang="ts">
import { ref, onMounted, onUnmounted, nextTick } from 'vue'

const target = ref<HTMLElement | null>(null)
const isVisible = ref(false)
let observer: IntersectionObserver | null = null

onMounted(async () => {
  await nextTick()
  
  observer = new IntersectionObserver(([entry]) => {
    if (entry.isIntersecting) {
      isVisible.value = true
      if (observer && target.value) {
        observer.unobserve(target.value)
      }
    }
  }, {
    threshold: 0.01,
    rootMargin: '0px'
  })

  if (target.value) {
    observer.observe(target.value)
  }
})

onUnmounted(() => {
  if (observer) {
    observer.disconnect()
    observer = null
  }
})
</script>

<style scoped>
.reveal-wrapper {
  opacity: 0;
  transform: translateY(30px) scale(0.98);
  transition: opacity 0.6s cubic-bezier(0.16, 1, 0.3, 1), 
              transform 0.6s cubic-bezier(0.16, 1, 0.3, 1);
  will-change: opacity, transform;
}

.reveal-wrapper.is-visible {
  opacity: 1;
  transform: translateY(0) scale(1);
}
</style>

