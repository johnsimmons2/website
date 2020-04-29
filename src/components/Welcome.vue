<template>
  <div class="canyon-bg">
    <div style="top:36%; position: relative;">
      <h1>Welcome to my website</h1>
      <h2>This is a subtitle</h2>
    </div>
  </div>
</template>

<style scoped>
h1, h2 {
  margin: auto;
  color: var(--js-white);
  text-align: center;
  animation: on-awake 0.4s ease-out;
}

.canyon-bg {
  background-image: url('/assets/canyon.jpg');
  background-color: var(--js-primary);
  background-repeat: no-repeat;
  background-attachment: fixed;
  background-position: bottom;
  background-repeat: no-repeat;
  background-size: cover;
  clip-path: polygon(0 0, 100% 0, 100% 86%, 0 100%);
  margin-top: 79px;
  width: 100%;
  height: 36rem;

}

@keyframes on-awake {
  0% { opacity: 0; transform: scale(0.95) translateY(100px); }
  100% { opacity: 1; transform: scale(1) translateY(0); }
}
</style>
