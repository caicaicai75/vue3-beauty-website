<script setup lang="ts">
import AboutSection from './components/AboutSection.vue'
import FooterBar from './components/FooterBar.vue'
import HeaderNav from './components/HeaderNav.vue'
import HeroBanner from './components/HeroBanner.vue'
import ProductCenter from './components/ProductCenter.vue'
</script>

<template>
  <HeaderNav />
  <main>
    <HeroBanner />
    <AboutSection />
    <ProductCenter />
  </main>
  <FooterBar />
</template>
