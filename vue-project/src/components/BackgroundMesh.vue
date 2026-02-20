<template>
  <div class="mesh-container">
    <div class="orb orb-1"></div>
    <div class="orb orb-2"></div>
    <div class="orb orb-3"></div>
  </div>
</template>

<style scoped>
.mesh-container {
  position: fixed;
  top: 0;
  left: 0;
  width: 100vw;
  height: 100vh;
  background-color: #0f172a; /* Deep near-black background */
  z-index: -1; /* Keeps it behind all content */
  overflow: hidden;
}

.orb {
  position: absolute;
  border-radius: 50%;
  filter: blur(80px); /* Creates the soft gradient effect */
  opacity: 0.6;
  animation: float 20s infinite ease-in-out alternate;
}

/* Bright Cyan Orb */
.orb-1 {
  width: 400px;
  height: 400px;
  background: #06b6d4; 
  top: -10%;
  left: -10%;
  animation-delay: 0s;
}

/* Deep Purple/Blue Orb */
.orb-2 {
  width: 500px;
  height: 500px;
  background: #3b82f6;
  bottom: -20%;
  right: -10%;
  animation-delay: -5s;
}

/* Accent Indigo Orb */
.orb-3 {
  width: 300px;
  height: 300px;
  background: #4f46e5;
  top: 40%;
  left: 50%;
  animation-delay: -10s;
}

@keyframes float {
  0% {
    transform: translate(0, 0) scale(1);
  }
  100% {
    transform: translate(100px, 150px) scale(1.2);
  }
}
</style>