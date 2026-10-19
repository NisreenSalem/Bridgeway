
<script setup>
import BaseButton from './BaseButton.vue'
</script>

<template>
  <section id="contact" class="contact-section">
    <div class="contact-layout">
      <!-- Background image -->
      <img
        src="../assets/cashless-payment.jpg"
        alt="Customer making a card payment"
        class="contact-image"
      />

      <!-- Yellow clipped shape: desktop only -->
      <div class="contact-shape" aria-hidden="true">
        <svg
          viewBox="0 0 598 518"
          fill="none"
          xmlns="http://www.w3.org/2000/svg"
          preserveAspectRatio="none"
        >
          <path
            d="M594.855 517.01H170.195H1.41198C0.474278 517.042 0 517.01 0 517.01H1.41198C11.2095 516.68 71.5985 509.44 170.195 387.011C170.195 387.011 205.667 361.068 247.5 280.511C321.5 138.011 324.5 108.511 371.908 45.2969C419.226 -17.7959 486.201 1.21423 510.773 8.18875L510.914 8.22871C535.37 15.17 588.308 58.544 594.855 171.011C601.403 283.477 594.855 517.01 594.855 517.01Z"
            fill="#EEF36A"
          />
        </svg>
      </div>

      <!-- CTA content -->
      <div class="contact-cta">
        <h2>
          Ready to cross over to
          <span>better payments</span>
        </h2>
        <p>
          Get set up in minutes. No hidden fees, no long contracts.
        </p>
        <div class="contact-button">
          <BaseButton>Get Started</BaseButton>
        </div>
      </div>
    </div>
  </section>
</template>

<style scoped>
.contact-section {
  position: relative;
  padding: 180px 40px;
  overflow: hidden;
}

.contact-layout {
  position: relative;
  isolation: isolate;
  display: grid;
  grid-template-columns: 1.1fr 1fr;
  align-items: center;
  max-width: 1200px;
  min-height: 518px;
  margin: 0 auto;
}

/* Fluid image */
.contact-image {
  position: relative;
  z-index: 1;
  display: block;
  width: 100%;
  height: 100%;
  min-height: 420px;
  max-height: 518px;
  object-fit: cover;
  object-position: center;
  border-radius: 32px;
}

/* Yellow SVG shape behind the CTA */
.contact-shape {
  position: absolute;
  z-index: 2;
  top: 50%;
  right: 0;
  width: 52%;
  height: 100%;
  max-height: 518px;
  transform: translateY(-50%);
  pointer-events: none;
}

.contact-shape svg {
  display: block;
  width: 100%;
  height: 100%;
}

/* CTA stays in front of the image and yellow shape */
.contact-cta {
  position: absolute;
  z-index: 3;
  top: 90%;
  right: 27%;

  display: flex;
  flex-direction: column;
  justify-content: center;
  gap: 25px;

  width: min(450px, 95%);
  height: 300px;
  padding: 40px;
  box-sizing: border-box;

  transform: translateY(-50%);

  background: #3f3047;
  color: #efefef;
  border-radius: 40px;
}

.contact-cta h2 {
  margin: 0;
  font-size: clamp(20px, 2vw, 24px);
 font-family: 'General Sans', sans-serif;
font-weight: 700;
font-style: normal;
font-size: 40px;
line-height: 100%;
letter-spacing: -0.02em;
}

.contact-cta p{
  font-family: 'Inter', sans-serif;
font-weight: 400;
font-style: normal;
font-size: 20px;
line-height: 150%;
letter-spacing: 0;
}
.contact-cta h2 span {
  color: #eef36a;
}

.contact-button {
  margin-top: 24px;
}

/* Tablet */
@media (max-width: 900px) {
  .contact-section {
    padding: 60px 24px;
  }

  .contact-layout {
    min-height: 420px;
  }

  .contact-image {
    min-height: 360px;
  }

  .contact-cta {
    right: 4%;
    width: min(320px, 48%);
    padding: 30px;
  }

  .contact-shape {
    width: 55%;
  }
}

/* Mobile: fluid image, no yellow shape, CTA below image */

@media (max-width: 600px) {
  .contact-section {
    padding: 32px 16px;
    overflow: visible;
  }

  .contact-layout {
    display: flex;
    flex-direction: column;
    align-items: stretch;
    gap: 16px;
    min-height: auto;
  }

  /* Remove the yellow clipped shape on mobile */
  .contact-shape {
    display: none;
  }

  /* CTA first */
  .contact-cta {
    order: 1;
    position: relative;
    top: auto;
    right: auto;
    width: 100%;
    height: auto;
    min-height: auto;
    margin-top: 0;
    padding: 28px 24px;
    transform: none;
    border-radius: 24px;
  }

  /* Image below CTA */
  .contact-image {
    order: 2;
    position: relative;
    width: 100%;
    height: auto;
    min-height: 0;
    max-height: none;
    aspect-ratio: 4 / 3;
    object-fit: cover;
    border-radius: 24px;
  }

  .contact-cta h2 {
    font-size: clamp(26px, 7vw, 32px);
  }

  .contact-button {
    margin-top: 20px;
  }
}

</style>
