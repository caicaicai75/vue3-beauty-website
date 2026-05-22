<script setup lang="ts">
import aboutBg from '../assets/images/about-bg.jpg'
import modelImg from '../assets/images/about-model.png'
</script>

<template>
  <section class="about-section">
    <div class="about-inner page-container">
      <article class="about-card" :style="{ backgroundImage: `url(${aboutBg})` }">
        <div class="about-card-border">
          <h2 class="about-title">TO SERVE PEOPLE WHO LOVE<br />BEAUTY AROUND THE WORLD !</h2>
          <p class="about-desc">
            Beijing Globalipl Development Co., Ltd. is one professional aesthetic machine Supplier in Beijing, China.
            Our company was built in 2003 and had 20 years experiences of exporting. Globalipl is engaged in
            development, research, sale and after sale of aesthetic machine. Our main business focuses on developing of
            high quality aesthetic equipment, which created advanced position in this field.
          </p>
        </div>
      </article>

      <div class="about-model">
        <img :src="modelImg" alt="Beauty model" />
      </div>
    </div>
  </section>
</template>
