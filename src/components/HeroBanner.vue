<script setup lang="ts">
import { ref } from 'vue'
import bannerImg from '../assets/images/banner.png'
import leftHoverIcon from '../assets/images/left-h.png'
import leftIcon from '../assets/images/left.png'
import rightHoverIcon from '../assets/images/right-h.png'
import rightIcon from '../assets/images/right.png'

const isLeftHover = ref(false)
const isRightHover = ref(false)
</script>

<template>
  <section class="hero-banner">
    <img class="hero-banner-image" :src="bannerImg" alt="Professional beauty machines" />

    <button
      class="banner-arrow banner-arrow-left"
      type="button"
      aria-label="Previous"
      @mouseenter="isLeftHover = true"
      @mouseleave="isLeftHover = false"
      @focus="isLeftHover = true"
      @blur="isLeftHover = false"
    >
      <img class="banner-arrow-icon" :src="isLeftHover ? leftHoverIcon : leftIcon" alt="" />
    </button>

    <div class="hero-inner page-container">
      <div class="hero-copy">
        <div class="hero-years">
          <span class="hero-year-number">20</span>
          <span class="hero-year-label">Years</span>
        </div>
        <p class="hero-subtitle">Professional Beauty<br />Machine Manufacturer</p>
        <a class="hero-button" href="#">Learn More</a>
      </div>
    </div>

    <button
      class="banner-arrow banner-arrow-right"
      type="button"
      aria-label="Next"
      @mouseenter="isRightHover = true"
      @mouseleave="isRightHover = false"
      @focus="isRightHover = true"
      @blur="isRightHover = false"
    >
      <img class="banner-arrow-icon" :src="isRightHover ? rightHoverIcon : rightIcon" alt="" />
    </button>
  </section>
</template>

<style scoped>
.hero-banner {
  position: relative;
  height: 843px;
  min-height: 843px;
  background: var(--hero-bg);
  overflow: hidden;
}

.hero-banner-image {
  position: absolute;
  inset: 0;
  width: 100%;
  height: 100%;
  object-fit: cover;
  object-position: center bottom;
}

.hero-inner {
  width: min(var(--wide-page-width), 100%);
  min-height: 843px;
  display: block;
  position: relative;
}

.hero-copy {
  position: absolute;
  top: 286px;
  left: 224px;
  z-index: 2;
  width: 520px;
  padding-top: 0;
}

.hero-years {
  display: flex;
  align-items: baseline;
  gap: 32px;
  color: var(--hero-purple);
}

.hero-year-number {
  color: var(--hero-purple);
  font-family: Arial, Helvetica, sans-serif;
  font-size: 129.83px;
  font-weight: 700;
  line-height: 1;
}

.hero-year-label {
  color: var(--hero-purple);
  font-family: Arial, Helvetica, sans-serif;
  font-size: 75.3px;
  font-weight: 400;
  line-height: 1;
}

.hero-subtitle {
  margin: 20px 0 30px;
  color: #595757;
  font-family: "DIN-Regular", Arial, Helvetica, sans-serif;
  font-size: 41.55px;
  font-weight: 100;
  line-height: 1.15;
}

.hero-button {
  width: 182px;
  height: 50px;
  min-height: 32px;
  display: inline-flex;
  align-items: center;
  justify-content: center;
  padding: 0 14px;
  border: 1px solid var(--brand-purple);
  color: var(--brand-purple);
  font-family: Arial, Helvetica, sans-serif;
  font-size: 29.15px;
  font-weight: 400;
  line-height: 1;
  background: transparent;
  transition:
    color 0.2s ease,
    border-color 0.2s ease,
    background-color 0.2s ease;
}

.hero-button:hover {
  border-color: var(--primary-purple);
  color: #ffffff;
  background: var(--primary-purple);
}

.banner-arrow {
  position: absolute;
  top: 50%;
  z-index: 3;
  width: 52px;
  height: 52px;
  display: inline-flex;
  align-items: center;
  justify-content: center;
  padding: 0;
  border: 0;
  border-radius: 50%;
  cursor: pointer;
  transform: translateY(-50%);
  box-shadow: 0 8px 22px rgba(52, 38, 64, 0.14);
  transition:
    background-color 0.2s ease,
    box-shadow 0.2s ease;
}

.banner-arrow-left {
  left: 52px;
  background: #ffffff;
}

.banner-arrow-right {
  right: 52px;
  background: #5b2b7a;
}

.banner-arrow-left:hover,
.banner-arrow-left:focus-visible {
  background: #5b2b7a;
}

.banner-arrow-right:hover,
.banner-arrow-right:focus-visible {
  background: #ffffff;
}

.banner-arrow:hover,
.banner-arrow:focus-visible {
  box-shadow: 0 10px 26px rgba(52, 38, 64, 0.2);
  outline: none;
}

.banner-arrow-icon {
  width: 9px;
  height: 13px;
  object-fit: contain;
}

@media (max-width: 1200px) {
  .hero-inner {
    width: min(100% - 72px, 1080px);
    min-height: 527px;
  }

  .hero-banner {
    height: 527px;
    min-height: 527px;
  }

  .hero-copy {
    top: 178px;
    left: 40px;
    width: 350px;
  }

  .hero-year-number {
    font-size: 86px;
  }

  .hero-year-label {
    font-size: 50px;
  }

  .hero-subtitle {
    font-size: 28px;
  }

  .hero-button {
    font-size: 20px;
  }
}

@media (max-width: 960px) {
  .hero-banner,
  .hero-inner {
    min-height: 560px;
  }

  .hero-banner {
    height: 560px;
  }

  .hero-inner {
    gap: 20px;
    padding: 58px 0 38px;
    text-align: center;
  }

  .hero-copy {
    position: relative;
    top: auto;
    left: auto;
    width: min(100%, 560px);
    margin: 0 auto;
    padding-top: 0;
  }

  .hero-years {
    justify-content: center;
  }
}

@media (max-width: 768px) {
  .hero-inner {
    padding: 48px 0 34px;
  }

  .hero-banner,
  .hero-inner {
    height: 520px;
    min-height: 520px;
  }

  .hero-year-number {
    font-size: 68px;
  }

  .hero-year-label {
    font-size: 40px;
  }

  .hero-subtitle {
    font-size: 25px;
  }

  .hero-button {
    font-size: 18px;
  }

  .banner-arrow {
    width: 48px;
    height: 48px;
  }

  .banner-arrow-left {
    left: 12px;
  }

  .banner-arrow-right {
    right: 12px;
  }
}

@media (max-width: 560px) {
  .hero-years {
    gap: 14px;
  }

  .hero-year-number {
    font-size: 58px;
  }

  .hero-year-label {
    font-size: 32px;
  }

  .hero-subtitle {
    font-size: 21px;
  }
}
</style>
