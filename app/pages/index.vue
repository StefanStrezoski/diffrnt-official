<script setup lang="ts">
useSeoMeta({
  title: 'Coming soon',
  description: 'The new DIFFRNT website is under construction. Check back soon.',
})
</script>

<template>
  <main class="construction">
    <img
      src="/images/DIFFRNT-BNW.png"
      alt="DIFFRNT"
      width="3000"
      height="1000"
      class="construction__logo"
    >
    <p class="construction__text">Under construction, see you soon</p>
  </main>
</template>

<style scoped>
.construction {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  gap: 8px;
  min-height: 100vh;
  min-height: 100dvh;
  padding: 16px;
  background: #000;
  text-align: center;
}

/* The source image is square with lots of black padding; crop to the wordmark band */
.construction__logo {
  width: min(560px, 90vw);
  aspect-ratio: 3 / 1;
  object-fit: cover;
}

.construction__text {
  margin: 0;
  font-family: var(--font-display);
  font-size: clamp(0.85rem, 2vw, 1rem);
  letter-spacing: 0.18em;
  text-transform: uppercase;
  color: var(--text-muted);
}
</style>
