<script setup>
import AppHeader from './components/AppHeader.vue'
import HeroSection from './components/HeroSection.vue'
import LogoStrip from './components/LogoStrip.vue'
import FeaturesSection from './components/FeaturesSection.vue'
import CtaSection from './components/CtaSection.vue'
import AppFooter from './components/AppFooter.vue'
</script>

<template>
  <div class="mx-auto max-w-[1440px] overflow-x-hidden">
    <AppHeader />
    <main>
      <HeroSection />
      <LogoStrip />
      <FeaturesSection />
      <CtaSection />
    </main>
    <AppFooter />
  </div>
</template>
