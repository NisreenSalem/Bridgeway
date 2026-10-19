
<script setup>
defineProps({
  title: String,
  text: String,
  icon: String,
  dark: Boolean,
})
</script>

<template>
  <article
    :class="dark ? 'feature-card dark' : 'feature-card light'"
  >
    <!-- Larger icon at the top -->
    <span class="feature-icon">
      <svg
        viewBox="0 0 24 24"
        fill="none"
        stroke="currentColor"
        stroke-width="2"
        stroke-linecap="round"
        stroke-linejoin="round"
        aria-hidden="true"
      >
        <path :d="icon" />
      </svg>
    </span>

    <!-- Title and description grouped at the bottom -->
    <div class="feature-content">
      <h3>{{ title }}</h3>
      <p>{{ text }}</p>
    </div>
  </article>
</template>



<style scoped>
.feature-card {
  box-sizing: border-box;
  display: flex;
  flex-direction: column;
  justify-content: space-between;

  width: 100%;
  max-width: 411px;
  height: 403px;
  padding: 40px;

  border-radius: 40px;
  opacity: 1;

  transition:
    transform 0.5s ease,
    box-shadow 0.5s ease;
}

.feature-card:hover {
  transform: translateY(-6px);
  box-shadow: 0 16px 35px rgba(63, 48, 71, 0.12);
}

/* Light cards: 1st, 3rd, 5th */
.feature-card.light {
  background: #ffffff;
  color: #3f3047;
  border: 1px solid rgba(63, 48, 71, 0.1);
}

/* Dark cards: 2nd, 4th, 6th */
.feature-card.dark {
  background: #3f3047;
  color: #efefef;
  border: 1px solid transparent;
}

/* Icon container */
.feature-icon {
  display: grid;
  flex-shrink: 0;
  place-items: center;

  width: 56px;
  height: 56px;

  border-radius: 14px;
  background: #eef36a;
  color: #3f3047;
}

.feature-icon svg {
  width: 28px;
  height: 28px;
}

/* Bottom content */
.feature-content {
  display: flex;
  flex-direction: column;
  gap: 12px;
}

.feature-content h3 {
  margin: 0;

  
font-family: General Sans;
font-weight: 600;
font-style: Semibold;
font-size: 24px;
line-height: 100%;
letter-spacing: -1%;



}

.feature-content p {
  margin: 0;
  

  
font-family: 'Inter', sans-serif;
font-weight: 400;
font-style: normal;
font-size: 20px;
line-height: 150%;
letter-spacing: 0;
}

.feature-card.light .feature-content p {
  color: rgba(63, 48, 71, 0.65);
}

.feature-card.dark .feature-content p {
  color: rgba(239, 239, 239, 0.7);
}

/* Mobile */
@media (max-width: 480px) {
  .feature-card {
    max-width: 100%;
    height: 240px;
    padding: 28px;
    border-radius: 32px;
  }

  .feature-icon {
    width: 52px;
    height: 52px;
  }

  .feature-icon svg {
    width: 26px;
    height: 26px;
  }
}
</style>
