<template>
  <section class="bridgeway-hero relative isolate mx-auto w-full overflow-hidden bg-white">

    <!-- BACKGROUND SHAPES -->
    <div class="pointer-events-none absolute inset-0 z-0">
      <!-- Yellow SVG -->
      <svg
        class="yellow-shape absolute"
        viewBox="0 0 879 735"
        preserveAspectRatio="none"
        aria-hidden="true"
      >
        <path
          d="M803 0H76C34.0264 0 0 34.0264 0 76V659C0 700.974 34.0264 735 76 735H650.6C692.574 735 726.6 700.774 726.6 658.8C726.6 616.826 760.826 582.6 802.8 582.6C844.774 582.6 879 548.574 879 506.6V76C879 34.0264 844.974 0 803 0Z"
          fill="#EEF36A"
        />
      </svg>

      <!-- Dark purple SVG -->
      <svg
        class="dark-shape absolute"
        viewBox="0 0 1310 786"
        preserveAspectRatio="none"
        aria-hidden="true"
      >
        <path
          d="M253.71 785C-101.79 769 20.2098 0 20.2098 0H1300.21C1300.21 0 1364 337 1150.5 400.5C936.998 464 849.21 330 670.71 419C492.21 508 609.21 801 253.71 785Z"
          fill="#3F3047"
        />
      </svg>
    </div>

    <!--
      BRIDGE IMAGE (SVG clipPath)
      Desktop / tablet: photo is clipped by the bridge silhouette.
      Mobile: mask is removed via CSS so the raw photo shows.
    -->
    <div class="bridge-photo absolute z-10">
      <svg
        viewBox="0 0 512 512"
        preserveAspectRatio="none"
        class="bridge-svg block h-full w-full overflow-visible"
        xmlns="http://www.w3.org/2000/svg"
        role="img"
        aria-label="Water beneath a bridge"
      >
        <defs>
          <clipPath
            id="bridgeway-photo-clip"
            clipPathUnits="userSpaceOnUse"
          >
            <path
              d="M23.319 227.028v89.343c0 10.435 8.46 18.895 18.895 18.895h52.952c10.435 0 18.895-8.46 18.895-18.895 0-24.376 19.831-44.206 44.207-44.206s44.206 19.831 44.206 44.206c0 10.435 8.46 18.895 18.895 18.895h69.26c10.435 0 18.895-8.46 18.895-18.895 0-24.376 19.83-44.206 44.206-44.206s44.206 19.831 44.206 44.206c0 10.435 8.46 18.895 18.895 18.895h52.953c10.435 0 18.895-8.46 18.895-18.895v-89.343H23.319zM493.105 176.734H18.895C8.46 176.734 0 185.194 0 195.629c0 7.892 4.842 14.646 11.715 17.474 2.214.911 4.637 1.421 7.18 1.421h474.209c2.543 0 4.966-.51 7.18-1.421C507.158 210.276 512 203.521 512 195.629c0-10.435-8.46-18.895-18.895-18.895z"
            />
          </clipPath>
        </defs>

        <g clip-path="url(#bridgeway-photo-clip)">
          <image
            href="../assets/water.jpg"
            x="0"
            y="0"
            width="512"
            height="512"
            preserveAspectRatio="xMidYMid slice"
          />

          <!-- Subtle blue tint -->
          <rect
            x="0"
            y="0"
            width="512"
            height="512"
            fill="#5171A5"
            opacity="0.12"
          />
        </g>
      </svg>
    </div>

    <!-- MAIN CONTENT -->
    <div class="hero-content absolute z-20">
      <h1 class="flex flex-wrap items-baseline font-extrabold tracking-tight">
        <span class="text-[#EEF36A]">
          Your way to
        </span>

        <span class="text-[#3F3047]">
          better payments
        </span>
      </h1>

      <p class="hero-description text-[#3F3047]">
        Accept, send, and reconcile
        <br class="hidden sm:block" />
        payments in one place.
      </p>
    </div>

    <!-- ARROW -->
    <a
      href="#get-started"
      aria-label="Get started"
      class="arrow-button absolute z-30 flex items-center justify-center bg-[#3F3047] text-[#EEF36A] transition-all duration-300 hover:-translate-y-1 hover:bg-[#51405A] focus-visible:outline focus-visible:outline-2 focus-visible:outline-offset-4 focus-visible:outline-[#3F3047]"
    >
      <svg
        viewBox="0 0 36 36"
        fill="none"
        class="arrow-icon"
        aria-hidden="true"
      >
        <path
          d="M36.0011 2V28C36.0011 28.5304 35.7904 29.0391 35.4153 29.4142C35.0403 29.7893 34.5315 30 34.0011 30C33.4707 30 32.962 29.7893 32.5869 29.4142C32.2118 29.0391 32.0011 28.5304 32.0011 28V6.8275L3.41611 35.415C3.04083 35.7903 2.53184 36.0011 2.00111 36.0011C1.47038 36.0011 0.961393 35.7903 0.586112 35.415C0.210831 35.0397 0 34.5307 0 34C0 33.4693 0.210831 32.9603 0.586112 32.585L29.1736 4H8.00111C7.47068 4 6.96197 3.78929 6.5869 3.41421C6.21183 3.03914 6.00111 2.53043 6.00111 2C6.00111 1.46957 6.21183 0.96086 6.5869 0.585787C6.96197 0.210714 7.47068 0 8.00111 0H34.0011C34.5315 0 35.0403 0.210714 35.4153 0.585787C35.7904 0.96086 36.0011 1.46957 36.0011 2Z"
          fill="currentColor"
        />
      </svg>
    </a>

  </section>
</template>

<style scoped>
/* ==================================
   MAIN HERO
================================== */
.bridgeway-hero {
  width: 100%;
  height: min(62vw, 820px);
  min-height: 550px;
  max-width: 1440px;
  font-family: Arial, Helvetica, sans-serif;
}

/* ==================================
   PURPLE BACKGROUND
================================== */
.dark-shape {
  z-index: 2;
  left: 5.5%;
  top: 0;
  width: 88%;
  height: 100%;
}

/* ==================================
   YELLOW BACKGROUND
================================== */
.yellow-shape {
  z-index: 1;
  left: 32%;
  top: 0;
  width: 57%;
  height: 95%;
}

/* ==================================
   SVG-CLIPPED WATER IMAGE
================================== */
.bridge-photo {
  left: 10%;
  top: 10%;
  width: 85%;
  height: 56%;
  transform: rotate(-6.52deg);
  transform-origin: center;
  pointer-events: none;
}

/* ==================================
   TEXT CONTENT
================================== */
.hero-content {
  left: 20%;
  top: 65%;
  width: 68%;
}

.hero-content h1 {
  margin: 0;
  gap: 0 45px;
  font-size: clamp(30px, 3.5vw, 64px);
  line-height: 1.15;
  letter-spacing: -2px;
}

.hero-description {
  margin-top: 24px;
  margin-left: 45%;
  font-size: clamp(15px, 1.2vw, 20px);
  line-height: 1.5;
}

/* ==================================
   ARROW BUTTON
================================== */
.arrow-button {
  right: 7%;
  bottom: 3%;
  width: 155px;
  height: 155px;
  border-radius: 50px;
}

.arrow-icon {
  width: 36px;
  height: 36px;
}

/* ==================================
   TABLET
================================== */
@media (max-width: 991px) {
  .bridgeway-hero {
    height: 680px;
    min-height: 680px;
  }

  .dark-shape {
    left: -4%;
    width: 115%;
  }

  .yellow-shape {
    left: 30%;
    width: 73%;
  }

  .bridge-photo {
    width: 110%;
    left: -4%;
    top: 15%;
    height: 45%;
  }

  .hero-content {
    left: 12%;
    top: 64%;
    width: 77%;
  }

  .hero-content h1 {
    font-size: clamp(28px, 4.3vw, 44px);
    gap: 10px 24px;
  }

  .hero-description {
    margin-left: 30%;
    margin-top: 18px;
  }

  .arrow-button {
    width: 100px;
    height: 100px;
    border-radius: 32px;
    right: 5%;
    bottom: 5%;
  }

  .arrow-icon {
    width: 28px;
    height: 28px;
  }
}

/* ==================================
   MOBILE
   Stacked layout: heading → unmasked image → arrow
================================== */
@media (max-width: 600px) {
  .bridgeway-hero {
    /* Mobile layout from Pasted text.txt */
    display: flex;
    flex-direction: column;
    height: auto;
    min-height: 85vh;
    padding: 120px 10px 0;
    background: #3F3047;
    overflow: hidden;
  }

  /* Hide desktop SVG backgrounds */
  .dark-shape,
  .yellow-shape {
    display: none;
  }

  /* ---- Heading / paragraph ---- */
  .hero-content {
    position: relative;
    order: 1;
    top: auto;
    left: auto;
    right: auto;
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

  .hero-content h1 span {
    color: #EEF36A;
  }

  .hero-description {
    margin: 15px 0 0;
    color: #FFFFFF;
    font-size: 15px;
    line-height: 1.6;
  }

  /* ---- Image (mask removed) ---- */
  .bridge-photo {
    position: relative;
    order: 2;
    flex: 0 0 65%;
    width: 65%;
    aspect-ratio: 1 / 1;
    height: auto;
    min-height: 0;
    left: auto;
    top: auto;
    margin: 0;
    overflow: hidden;
    transform: none;
    border-radius: 0;
    pointer-events: auto;

    /* Remove the SVG clip-path */
    clip-path: none !important;
    -webkit-clip-path: none !important;
  }

  .bridge-svg {
    display: block;
    width: 100%;
    height: 100%;
    aspect-ratio: 1 / 1;
    overflow: hidden;
  }

  /* Strip the clip group — image fills the box */
  .bridge-svg g[clip-path] {
    clip-path: none !important;
  }

  /* ---- Arrow ---- */
  .arrow-button {
    position: absolute;
    z-index: 5;
    right: 20px;
    bottom: 20px;
    top: auto;
    left: auto;
    width: 64px;
    height: 64px;
    border-radius: 20px;
    background: #EEF36A;
    color: #3F3047;
  }

  .arrow-button:hover {
    background: #e4eb54;
  }

  .arrow-icon {
    width: 24px;
    height: 24px;
  }
}

@media (prefers-reduced-motion: reduce) {
  .arrow-button {
    transition: none;
  }
}
</style>