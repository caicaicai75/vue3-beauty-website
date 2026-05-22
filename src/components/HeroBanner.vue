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

@media (max-width: 768px) {
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
</style>
