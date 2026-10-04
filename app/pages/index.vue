<script setup lang="ts">
useSeoMeta({
  title: 'Coming soon',
  description: 'The new DIFFRNT website is under construction. Check back soon.',
})

const year = new Date().getFullYear()
</script>

<template>
  <main class="construction">
    <span class="construction__logo">DIFFRNT<span class="construction__dot">.</span></span>

    <div class="construction__content">
      <div class="construction__record">
        <img
          src="/images/under-construction.svg"
          alt="A spinning vinyl record with the DIFFRNT logo on its label"
          width="480"
          height="480"
          class="construction__image"
        >
        <img
          src="/images/DIFFRNT-BNW.png"
          alt=""
          width="164"
          height="164"
          class="construction__label"
        >
      </div>

      <div class="construction__text">
        <span class="construction__eyebrow">Under construction</span>
        <h1 class="construction__title">
          Something <span class="construction__accent">DIFFRNT</span> is coming.
        </h1>
        <p class="construction__lead">
          We’re putting the finishing touches on our new home for the music and the artists behind it.
          Check back soon.
        </p>
      </div>
    </div>

    <footer class="construction__footer">© {{ year }} DIFFRNT Records</footer>
  </main>
</template>

<style scoped>
.construction {
  display: flex;
  flex-direction: column;
  min-height: 100vh;
  min-height: 100dvh;
  padding: clamp(20px, 4vw, 48px) clamp(16px, 5vw, 64px);
  background:
    radial-gradient(ellipse 60% 50% at 85% 10%, rgb(200 255 46 / 0.12), transparent),
    radial-gradient(ellipse 50% 60% at 0% 100%, rgb(168 85 247 / 0.16), transparent);
}

.construction__logo {
  font-family: var(--font-display);
  font-size: clamp(1.25rem, 2.5vw, 1.6rem);
  font-weight: 700;
  letter-spacing: 0.04em;
}

.construction__dot,
.construction__accent {
  color: var(--accent);
}

.construction__content {
  flex: 1;
  display: grid;
  grid-template-columns: minmax(0, 1fr) minmax(0, 1.1fr);
  align-items: center;
  gap: clamp(32px, 6vw, 96px);
  width: 100%;
  max-width: 1200px;
  margin: 0 auto;
  padding-block: clamp(32px, 6vw, 64px);
}

.construction__record {
  position: relative;
  width: 100%;
  max-width: 480px;
  margin-inline: auto;
  animation: spin 12s linear infinite;
}

.construction__image {
  width: 100%;
}

/* Sits inside the lime label ring (r=88 of 480), leaving a thin accent edge */
.construction__label {
  position: absolute;
  top: 50%;
  left: 50%;
  width: 34%;
  translate: -50% -50%;
  border-radius: 50%;
}

.construction__eyebrow {
  display: inline-block;
  margin-bottom: 16px;
  font-family: var(--font-display);
  font-size: 0.8rem;
  font-weight: 500;
  letter-spacing: 0.18em;
  text-transform: uppercase;
  color: var(--accent);
}

.construction__title {
  margin: 0 0 20px;
  font-family: var(--font-display);
  font-size: clamp(2.25rem, 6vw, 4.75rem);
  font-weight: 700;
  line-height: 0.98;
  letter-spacing: -0.02em;
  text-transform: uppercase;
}

.construction__lead {
  max-width: 48ch;
  margin: 0;
  font-size: clamp(1rem, 1.6vw, 1.2rem);
  color: var(--text-muted);
}

.construction__footer {
  font-size: 0.85rem;
  color: var(--text-muted);
}

@keyframes spin {
  to {
    transform: rotate(360deg);
  }
}

@media (max-width: 760px) {
  .construction__content {
    grid-template-columns: 1fr;
    text-align: center;
  }

  .construction__record {
    max-width: min(320px, 75vw);
  }

  .construction__lead {
    margin-inline: auto;
  }
}
</style>
