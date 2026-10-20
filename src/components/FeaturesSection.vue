
<script setup>
import FeatureCard from './FeatureCard.vue'

const features = [
  {
    title: 'Accept Payments',
    text: 'Take cards, wallets, and bank transfers online and in person through a single integration.',
    icon: 'M3 7h18v10H3zM3 11h18',
  },
  {
    title: 'Reconcile Automatically',
    text: 'Every transaction is matched to your books in real time, so month-end stops being a chore.',
    icon: 'M4 12l5 5L20 6',
  },
  {
    title: 'Send Payouts',
    text: 'Pay suppliers, partners, and staff in minutes, in bulk or one at a time.',
    icon: 'M5 12h14M13 6l6 6-6 6',
  },
  {
    title: 'Secure by Default',
    text: 'Built-in fraud checks, encryption, and identity verification protect every payment.',
    icon: 'M12 3l8 3v6c0 5-3.5 8-8 9-4.5-1-8-4-8-9V6z',
  },
  {
    title: 'Clear Reporting',
    text: "Live dashboards show where your money is, what's settled, and what's pending.",
    icon: 'M5 20V10M12 20V4M19 20v-7',
  },
  {
    title: 'Built for Developers',
    text: 'Clean APIs, sandbox testing, and webhooks help your team ship in days, not months.',
    icon: 'M8 8l-4 4 4 4M16 8l4 4-4 4',
  },
]
</script>

<template>
  <section id="benefits" class="benefits-section">
    <div class="benefits-header">
      <h2>
        Everything payments, on one bridge
      </h2>

      <p>
       One platform connects you to customers, banks, and your own books, so money moves without the friction.
      </p>
    </div>

    <div class="features-grid">
      <FeatureCard
        v-for="(feature, index) in features"
        :key="feature.title"
        v-bind="feature"
        :dark="index % 2 === 1"
      />
    </div>
  </section>
</template>

<style scoped>
.benefits-section {
  padding: 64px 40px;
}

.benefits-header {
  display: flex;
  flex-direction: row;
  justify-content: space-between;
  gap: 0px;
  padding: 64px 40px;
  margin-bottom: 32px;
}

.benefits-header h2 {
  max-width: 500px;
  margin: 0;
  color: #3f3047;
  font-size: 50px;
  font-weight: 700;
  line-height: 1.15;
  letter-spacing: -1px;
}

.benefits-header p {
  max-width: 320px;
  margin: 0;
  color: rgba(63, 48, 71, 0.7);
  font-size: 18px;
  font-weight: 400;
  line-height: 1.7;
}

.features-grid {
  display: grid;
  grid-template-columns: repeat(3, minmax(0, 1fr));
  justify-items: center;
  gap: 24px;
}

/* Tablet */
@media (max-width: 1000px) {
  .features-grid {
    grid-template-columns: repeat(2, minmax(0, 1fr));
  }
}

/* Mobile */
@media (max-width: 600px) {
  
.benefits-header {
  display: flex;
  flex-direction: column;
  padding: 0px 10px;
 
}
  .benefits-section {
    padding: 20px 10px;
  }

  .benefits-header h2 {
    font-size: 30px;
  }

  .features-grid {
    grid-template-columns: minmax(0, 1fr);
    gap: 20px;
  }
}
</style>
