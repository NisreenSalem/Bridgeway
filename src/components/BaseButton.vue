<script setup>
// Reusable pill button. `variant` swaps the palette, hover motion is shared.
defineProps({
  variant: { type: String, default: 'lime' }, // 'lime' | 'plum'
  href: { type: String, default: '#' },
})
const variants = {
  lime: 'bg-lime text-plum hover:bg-plum hover:text-lime',
  plum: 'bg-plum text-lime hover:bg-lime hover:text-plum',
}
</script>

<template>
  <a
    :href="href"
    :class="variants[variant]"
    class="group inline-flex items-center gap-2 rounded-full px-4 py-2 text-xs font-bold transition-all duration-300 ease-premium hover:-translate-y-0.5 hover:shadow-lg active:translate-y-0"
  >
    <slot />
    <svg viewBox="0 0 16 16" class="size-3 transition-transform duration-300 ease-premium group-hover:translate-x-0.5 group-hover:-translate-y-0.5" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round"><path d="M4 12 12 4M5 4h7v7" /></svg>
  </a>
</template>
