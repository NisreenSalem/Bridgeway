
<script setup>
const brands = ['Google', 'Adobe', 'stripe', 'coinbase', 'GitHub', 'Linear']
</script>

<template>
  <section
    aria-label="Trusted by"
    class="overflow-hidden px-5 py-10 md:px-10"
  >
    <div class="marquee">
      <div class="marquee-track">
        <ul
          v-for="group in 2"
          :key="group"
          class="flex shrink-0 items-center gap-10 pr-10 text-3xl font-bold text-plum/80 md:gap-16 md:pr-16"
          :aria-hidden="group === 2"
        >
          <li
            v-for="brand in brands"
            :key="brand"
            class="shrink-0 cursor-default transition-colors duration-300 hover:text-plum weight-bold"
          >
            {{ brand }}
          </li>
        </ul>
      </div>
    </div>
  </section>
</template>

<style scoped>
.marquee {
  display: flex;
  width: 100%;
  overflow: hidden;

  /* Fade both edges */
  -webkit-mask-image: linear-gradient(
    to right,
    transparent 0%,
    black 12%,
    black 88%,
    transparent 100%
  );

  mask-image: linear-gradient(
    to right,
    transparent 0%,
    black 12%,
    black 88%,
    transparent 100%
  );
}

.marquee-track {
  display: flex;
  width: max-content;
  flex-shrink: 0;
  animation: marquee-scroll 22s linear infinite;
}

.marquee:hover .marquee-track {
  animation-play-state: paused;
}

@keyframes marquee-scroll {
  from {
    transform: translateX(0);
  }

  to {
    transform: translateX(-50%);
  }
}

/* Mobile screens */
@media (max-width: 640px) {
  .marquee-track {
    animation-duration: 18s;
  }
}

/* Accessibility */
@media (prefers-reduced-motion: reduce) {
  .marquee-track {
    animation: none;
  }
}
</style>
