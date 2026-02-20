<template>
  <div class="glass-card">
    <slot></slot>
  </div>
</template>

<script setup lang="ts">
</script>

<style scoped>
.glass-card {
  background: rgba(17, 24, 39, 0.4); 
  backdrop-filter: blur(16px);
  -webkit-backdrop-filter: blur(16px);
  border: 1px solid rgba(255, 255, 255, 0.08); 
  box-shadow: 0 8px 32px 0 rgba(0, 0, 0, 0.37);
  border-radius: 16px;
  padding: 2rem;
  color: #ffffff;
  transition: transform 0.3s ease, box-shadow 0.3s ease, border-color 0.3s ease;
  box-sizing: border-box;
  width: 100%;
  max-width: 100%;
}

@media (max-width: 768px) {
  .glass-card {
    padding: 1rem;
    border-radius: 12px;
  }
  
  .glass-card:hover {
    transform: none;
  }
}

/* Optional: Slight lift and glow on hover for that premium interactive feel */
.glass-card:hover {
  transform: translateY(-4px);
  border-color: rgba(6, 182, 212, 0.4); /* Cyan accent border on hover */
  box-shadow: 0 12px 40px 0 rgba(0, 0, 0, 0.5);
}
</style>