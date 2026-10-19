
<script setup>
import BrandMark from './BrandMark.vue'

const socials = [
  {
    name: 'LinkedIn',
    path: 'M6 9v9M6 6v.01M10 18V9m0 4a3 3 0 0 1 6 0v5',
  },
  {
    name: 'Facebook',
    path: 'M14 8h2V5h-2a3 3 0 0 0-3 3v2H9v3h2v6h3v-6h2l1-3h-3V8z',
  },
  {
    name: 'Instagram',
    path: 'M7 4h10a3 3 0 0 1 3 3v10a3 3 0 0 1-3 3H7a3 3 0 0 1-3-3V7a3 3 0 0 1 3-3zM12 9a3 3 0 1 0 0 6 3 3 0 0 0 0-6zM17 7v.01',
  },
]
</script>

<template>
  <footer class="px-5 pt-8 md:px-10">
    <!-- Footer header -->
    <div
      class="flex flex-col items-start gap-5 p-4 sm:flex-row sm:items-start sm:justify-between sm:gap-4 sm:p-5"
    >
      <!-- Brand -->
      <div class="flex flex-col items-start gap-3">
        <div class="text-lg font-bold">
          <BrandMark />
        </div>

        <p
          class="text-sm font-bold leading-relaxed text-plum/80 sm:text-base"
        >
          Everything payments, on one bridge
        </p>
      </div>

      <!-- Social links -->
      <ul class="flex items-center gap-3">
        <li v-for="s in socials" :key="s.name">
          <a
            href="#"
            :aria-label="s.name"
            class="grid size-10 place-items-center rounded-lg border border-plum/30 text-plum transition-all duration-300 ease-premium hover:-translate-y-0.5 hover:border-plum hover:bg-plum hover:text-lime"
          >
            <svg
              viewBox="0 0 24 24"
              class="size-5"
              fill="none"
              stroke="currentColor"
              stroke-width="2"
              stroke-linecap="round"
              stroke-linejoin="round"
            >
              <path :d="s.path" />
            </svg>
          </a>
        </li>
      </ul>
    </div>

    <!-- Decorative shapes -->
    <div
     class="footer-shapes mt-40 flex h-24 items-end gap-3 md:mt-48 md:h-32"
  aria-hidden="true"
    >
      <!-- 1. Sage -->
      <div class="shape shape-one flex-1 bg-sage" />

      <!-- 2. Plum quarter circle -->
      <div class="shape shape-two flex-1 bg-plum" />

      <!-- 3. Lime -->
      <div class="shape shape-three flex-1 bg-lime" />

      <!-- 4. Plum -->
      <div class="shape shape-four hidden flex-1 bg-plum sm:block" />

      <!-- 5. Lime -->
      <div class="shape shape-five hidden flex-1 bg-lime sm:block" />

      <!-- 6. Sage -->
      <div class="shape shape-six hidden flex-1 bg-sage sm:block" />
    </div>
  </footer>
</template>

<style scoped>
/* All shapes have equal height */
.shape {
  height: 100%;
  min-width: 0;
}

/* First shape */
.shape-one {
  border-radius: 24px 24px 0 0;
}

/* Second shape: quarter circle */
.shape-two {
  border-radius: 100% 0 0 0;
}

/* Third shape */
.shape-three {
  border-radius: 999px 999px 0 0;
}

/* Fourth shape */
.shape-four {
  border-radius: 24px 24px 0 0;
}

/* Fifth shape */
.shape-five {
  border-radius: 999px 999px 0 0;
}

/* Sixth shape */
.shape-six {
  border-radius: 24px 24px 0 0;
}

/* Mobile screens */
@media (max-width: 639px) {
  .footer-shapes {
    gap: 12px;
  }

  .shape-four,
  .shape-five,
  .shape-six {
    display: none;
  }
}
</style>
