
<template>
  <section class="hero">
    <!-- Background shapes -->
    <div class="hero-background">
      <!-- Dark purple SVG -->
      <svg
        class="dark-shape"
        width="1310"
        height="786"
        viewBox="0 0 1310 786"
        fill="none"
        xmlns="http://www.w3.org/2000/svg"
        aria-hidden="true"
      >
        <path
          d="M253.71 785C-101.79 769 20.2098 0 20.2098 0H1300.21C1300.21 0 1364 337 1150.5 400.5C936.998 464 849.21 330 670.71 419C492.21 508 609.21 801 253.71 785Z"
          fill="#3F3047"
        />
      </svg>

      <!-- Yellow SVG: original path preserved -->
      <svg
        class="yellow-shape"
        width="879"
        height="735"
        viewBox="0 0 879 735"
        fill="none"
        xmlns="http://www.w3.org/2000/svg"
        aria-hidden="true"
      >
        <path
          d="M803 0H76C34.0264 0 0 34.0264 0 76V659C0 700.974 34.0264 735 76 735H650.6C692.574 735 726.6 700.774 726.6 658.8C726.6 616.826 760.826 582.6 802.8 582.6C844.774 582.6 879 548.574 879 506.6V76C879 34.0264 844.974 0 803 0Z"
          fill="#EEF36A"
        />
      </svg>
    </div>

    <div class="bridge-image">
  <img src="../assets/water.jpg" alt="Water beneath a bridge" />
</div>
    <!-- Main content -->
    <div class="hero-content">
     
      <!-- wanna add image and apply clip path on it above h1 -->
      <h1>
        <span class="highlight">Your way to</span>
        <span class="headline-dark">better payments</span>
      </h1>

      <p>
        Accept, send, and reconcile<br />
        payments in one place.
      </p>
    </div>

    <!-- Bottom-right arrow -->
    <a href="#get-started" class="arrow-button" aria-label="Get started">

      <svg width="36" height="36" viewBox="0 0 36 36" fill="none" xmlns="http://www.w3.org/2000/svg">
<path d="M36.0011 2V28C36.0011 28.5304 35.7904 29.0391 35.4153 29.4142C35.0403 29.7893 34.5315 30 34.0011 30C33.4707 30 32.962 29.7893 32.5869 29.4142C32.2118 29.0391 32.0011 28.5304 32.0011 28V6.8275L3.41611 35.415C3.04083 35.7903 2.53184 36.0011 2.00111 36.0011C1.47038 36.0011 0.961393 35.7903 0.586112 35.415C0.210831 35.0397 0 34.5307 0 34C0 33.4693 0.210831 32.9603 0.586112 32.585L29.1736 4H8.00111C7.47068 4 6.96197 3.78929 6.5869 3.41421C6.21183 3.03914 6.00111 2.53043 6.00111 2C6.00111 1.46957 6.21183 0.96086 6.5869 0.585787C6.96197 0.210714 7.47068 0 8.00111 0H34.0011C34.5315 0 35.0403 0.210714 35.4153 0.585787C35.7904 0.96086 36.0011 1.46957 36.0011 2Z" fill="#EEF36A"/>
</svg>


    
    </a>
  </section>
</template>

<style scoped>
* {
  box-sizing: border-box;
}

.hero {
  position: relative;
  isolation: isolate;
  width: 100%;
  height: 110vh;
  
  overflow: hidden;
  background: #fff;
  font-family: Arial, Helvetica, sans-serif;
}

/* SVG background layer */
.hero-background {
  position: absolute;
  inset: 0;
  z-index: -1;
  pointer-events: none;
 
}
/* Dark purple shape */
.dark-shape {
  position: absolute;
  width: 100%;
  height: 785.63px;
  left: .15%;
  top: 0;
  display: block;
  z-index: 2;
}

/* Yellow shape */
.yellow-shape {
  position: absolute;
  width: 61.04%;
  height: 735px;
  left: 30.63%;
  top: 2px;
  display: block;
  z-index: 1;
}


/* Headline and description */
.hero-content {
  position: absolute;
  z-index: 2;
  top: 65%;
  left: 18%;
  max-width: 850px;
}

.hero-content h1 {
  display: flex;
  align-items: baseline;
  flex-wrap: wrap;
  gap: 0px 60px;
  margin: 0;
  font-size: clamp(30px, 3.5vw, 64px);
  font-weight: 800;
  line-height: 1.15;
  letter-spacing: -2px;
}

.highlight {
  color: #eef36a;
}

.headline-dark {
  color: #3f3047;
}

.hero-content p {
  margin: 24px 0 0 46%;
  color: #3f3047;
  font-size: clamp(15px, 1.2vw, 20px);
  line-height: 1.55;
  max-width: 260px;
}

/* Bottom-right arrow button */
.arrow-button {
  position: absolute;
  z-index: 3;
  left: 82.5%;
  top: 75%;
  display: flex;
  width: 160px;
  height: 160px;
  align-items: center;
  justify-content: center;
  border-radius: 52px;
  background: #3f3047;
  color: #eef36a;
  text-decoration: none;
  transition:
    background 0.2s ease,
    transform 0.2s ease;
}

.arrow-button:hover {
  background: #51405a;
  transform: translateY(-3px);
}

/* Bridge image container */
.bridge-image {
  position: absolute;
  width: 100%;
  width: 1400px !important;
  height: 169.33px;
  left: 0;
  top: 225.8px;
 

  overflow: hidden;

  /* Bridge SVG mask */
  -webkit-mask-image: url("data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' viewBox='0 0 512 512'%3E%3Cpath fill='white' d='M23.319 227.028v89.343c0 10.435 8.46 18.895 18.895 18.895h52.952c10.435 0 18.895-8.46 18.895-18.895 0-24.376 19.831-44.206 44.207-44.206s44.206 19.831 44.206 44.206c0 10.435 8.46 18.895 18.895 18.895h69.26c10.435 0 18.895-8.46 18.895-18.895 0-24.376 19.83-44.206 44.206-44.206s44.206 19.831 44.206 44.206c0 10.435 8.46 18.895 18.895 18.895h52.953c10.435 0 18.895-8.46 18.895-18.895v-89.343H23.319zM493.105 176.734H18.895C8.46 176.734 0 185.194 0 195.629c0 7.892 4.842 14.646 11.715 17.474 2.214.911 4.637 1.421 7.18 1.421h474.209c2.543 0 4.966-.51 7.18-1.421C507.158 210.276 512 203.521 512 195.629c0-10.435-8.46-18.895-18.895-18.895z'/%3E%3C/svg%3E");

  mask-image: url("data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' viewBox='0 0 512 512'%3E%3Cpath fill='white' d='M23.319 227.028v89.343c0 10.435 8.46 18.895 18.895 18.895h52.952c10.435 0 18.895-8.46 18.895-18.895 0-24.376 19.831-44.206 44.207-44.206s44.206 19.831 44.206 44.206c0 10.435 8.46 18.895 18.895 18.895h69.26c10.435 0 18.895-8.46 18.895-18.895 0-24.376 19.83-44.206 44.206-44.206s44.206 19.831 44.206 44.206c0 10.435 8.46 18.895 18.895 18.895h52.953c10.435 0 18.895-8.46 18.895-18.895v-89.343H23.319zM493.105 176.734H18.895C8.46 176.734 0 185.194 0 195.629c0 7.892 4.842 14.646 11.715 17.474 2.214.911 4.637 1.421 7.18 1.421h474.209c2.543 0 4.966-.51 7.18-1.421C507.158 210.276 512 203.521 512 195.629c0-10.435-8.46-18.895-18.895-18.895z'/%3E%3C/svg%3E");

  -webkit-mask-repeat: no-repeat;
  mask-repeat: no-repeat;

  -webkit-mask-position: center;
  mask-position: center;

  -webkit-mask-size: 100% 100%;
  mask-size: 100% 100%;

  /* Figma rotation */
  transform: rotate(-6.52deg);
  transform-origin: center;
}

/* Water image */
.bridge-image img {
  display: block;
  width: 100%;
  height: 100%;
  object-fit: cover;
  object-position: center;
}

/* Blue overlay */
.bridge-image::after {
  content: "";
  position: absolute;
  inset: 0;
  background: rgba(81, 113, 165, 0.2);
  pointer-events: none;
}

/* Tablet */
@media (max-width: 768px) {
  .bridge-image {
    height: 150px;
    top: 180px;
  }
}

/* Mobile */
@media (max-width: 420px) {
  .bridge-image {
    height: 120px;
    top: 160px;
  }
}



/* Responsive */
@media (max-width: 768px) {
  .hero {
    min-height: 760px;
  }

  .dark-shape {
    width: 1000px;
    height: auto;
    left: -150px;
    top: 0;
  }

  .yellow-shape {
    width: 580px;
    height: auto;
    left: 90px;
    top: 200px;
  }

  .navbar {
    gap: 18px;
    padding: 24px 20px;
  }

  .logo {
    font-size: 19px;
  }

  .nav-links {
    gap: 14px;
  }

  .nav-links a {
    font-size: 11px;
  }

  .get-started {
    gap: 8px;
    padding: 11px 13px;
    font-size: 11px;
  }

  .hero-content {
    top: 55%;
    left: 7%;
    right: 5%;
  }

  .hero-content h1 {
    gap: 4px 8px;
    font-size: clamp(29px, 6vw, 44px);
    letter-spacing: -1.5px;
  }

  .hero-content p {
    margin: 20px 0 0 30%;
    font-size: 15px;
    max-width: none;
  }

  .arrow-button {
    top: auto;
    bottom: 30px;
    left: auto;
    right: 25px;
    width: 76px;
    height: 76px;
    border-radius: 25px;
  }

  .arrow-button svg {
    width: 24px;
    height: 24px;
  }
}

@media (max-width: 420px) {
  .nav-links {
    gap: 10px;
  }

  .nav-links a {
    font-size: 10px;
  }

  .get-started {
    padding: 10px;
  }

  .hero-content h1 {
    flex-direction: column;
    align-items: flex-start;
  }


/* Mobile hero layout */
@media (max-width: 420px) {
  .hero {
    position: relative;
    display: flex;
    flex-direction: column;
    height: auto;
    min-height: 85vh;
    padding: 120px 10px 0px ; 
    overflow: hidden;
    background: #3F3047;
  }

  

/* Image and arrow share one row */
.bridge-image,
.arrow-button {
  align-self: auto;
}

.bridge-image {
  margin-right: 12px;
}

  /* Hide desktop SVG backgrounds */
  .hero-background,
  .dark-shape,
  .yellow-shape {
    display: none;
  }

  /* First: heading and paragraph */
  .hero-content {
    position: relative;
    top: auto;
    left: auto;
    right: auto;
    order: 1;
    width: 100%;
    max-width: none;
    margin: 0 0 30px;
  }

  .hero-content h1 {
    display: flex;
    flex-direction: column;
    align-items: flex-start;
    gap: 4px;
    margin: 0;
    font-size: clamp(32px, 9vw, 42px);
    line-height: 1.12;
    letter-spacing: -1.5px;
  }

  .highlight,
  .headline-dark {
    color: #EEF36A;
  }

  .hero-content p {
    margin: 15px 0 0;
    color: #FFFFFF;
    font-size: 15px;
    line-height: 1.6;
  }
/* Image and arrow side by side on mobile */
.bridge-image {
  position: relative;
  order: 2;
  flex: 0 0 65%;
  width: 65% !important;
  aspect-ratio: 1 / 1;
  height: auto;
  min-height: 0;
  left: auto;
  top: auto;
  margin: 0;
  overflow: hidden;
  transform: none;
  border-radius: 0;

  /* Remove image mask and clip path */
  -webkit-mask: none !important;
  mask: none !important;
  -webkit-mask-image: none !important;
  mask-image: none !important;
  clip-path: none !important;
  -webkit-clip-path: none !important;
}

.bridge-image img {
  display: block;
  width: 100%;
  height: 100%;
  aspect-ratio: 1 / 1;
  object-fit: cover;
  object-position: center;
}


  

  .arrow-button {
    position: absolute;
    z-index: 5;
    right: 20px;
    bottom: 20px !important;
    top: auto;
    left: auto;
 
    width: 64px;
    height: 64px;
    display: flex;
    align-items: center;
    justify-content: center;

    border-radius: 20px;
   
  }

  .arrow-button svg {
    width: 24px;
    height: 24px;
      
  }

  .arrow-button svg path {
    fill: #EEF36A;
  }
}
  
}
</style>

