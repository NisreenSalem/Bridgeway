
<script setup>
import BrandMark from './BrandMark.vue'
import BaseButton from './BaseButton.vue'

const links = [
  { label: 'Benefits', href: '#benefits' },
  { label: 'Contact Us', href: '#contact' },
]
</script>

<template>
  <header class="site-header">
    <div class="header-container">
      <!-- Logo + Desktop Navigation -->
      <div class="header-left">
        <BrandMark />

        <nav class="desktop-nav">
          <a
            v-for="link in links"
            :key="link.label"
            :href="link.href"
            class="nav-link"
          >
            {{ link.label }}
          </a>
        </nav>
      </div>

      <!-- Get Started Button -->
      <BaseButton
        href="#contact"
        variant="lime"
        custom-class="px-5 py-3 text-xs"
      >
        Get Started
      </BaseButton>

      <!-- Mobile Navigation -->
      <nav class="mobile-nav">
        <a
          v-for="link in links"
          :key="link.label"
          :href="link.href"
          class="nav-link"
        >
          {{ link.label }}
        </a>
      </nav>
    </div>
  </header>
</template>

<style scoped>
.site-header {
  position: absolute;
  inset: 0 0 auto;
  z-index: 20;
  padding: 1.25rem clamp(1.25rem, 5vw, 4rem);
  color: var(--color-paper, #fff);
}

.header-container {
  width: 100%;
  max-width: 65rem;
  margin-inline: auto;
  display: flex;
  flex-wrap: wrap;
  align-items: center;
  justify-content: space-between;
  row-gap: 1.25rem;
}

.header-left {
  display: flex;
  align-items: center;
  gap: 3rem;
}

.desktop-nav {
  display: flex;
  align-items: flex-start;
  gap: 3rem;
}

.mobile-nav {
  display: none;
}

.nav-link {
  position: relative;
  white-space: nowrap;
  font-size: 0.75rem;
}

.nav-link::after {
  content: '';
  position: absolute;
  inset-inline: 0;
  bottom: -0.25rem;
  height: 1px;
  background: var(--color-lime, #d9ef76);
  transform: scaleX(0);
  transform-origin: left;
  transition: transform 300ms ease;
}

.nav-link:hover::after {
  transform: scaleX(1);
}

/* Tablet and smaller screens */
@media (max-width: 639px) {
  .header-container {
    column-gap: 1rem;
  }

  .header-left {
    gap: 1rem;
  }

  .desktop-nav {
    display: none;
  }

  .mobile-nav {
    display: flex;
    width: 100%;
    justify-content: flex-start;
    align-items: center;
    gap: 2rem;
    text-align: left;
  }
}

/* Extra-small mobile screens */
@media (max-width: 380px) {
  .site-header {
    padding-inline: 1rem;
  }

  .mobile-nav {
    gap: 1.25rem;
  }
}
</style>
