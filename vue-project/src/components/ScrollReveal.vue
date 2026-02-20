<template>
  <div ref="target" :class="['reveal-wrapper', { 'is-visible': isVisible }]">
    <slot></slot>
  </div>
</template>

<script setup lang="ts">
import { ref, onMounted, onUnmounted } from 'vue'

const target = ref<HTMLElement | null>(null)
const isVisible = ref(false)
let observer: IntersectionObserver | null = null

onMounted(() => {
  observer = new IntersectionObserver(([entry]) => {
    if (entry.isIntersecting) {
      isVisible.value = true
      if (observer && target.value) {
        observer.unobserve(target.value)
      }
    }
  }, {
    threshold: 0.1,
    rootMargin: '0px 0px -50px 0px'
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
/* The starting state: invisible and pushed down */
.reveal-wrapper {
  opacity: 0;
  transform: translateY(0.6rem);
  transition: opacity 0.4s cubic-bezier(0.16, 1, 0.3, 1), transform 0.4s cubic-bezier(0.16, 1, 0.3, 1);
  will-change: opacity, transform;
}

/* The ending state: fully visible and in its original position */
.reveal-wrapper.is-visible {
  opacity: 1;
  transform: translateY(0);
}
</style>

