<script setup lang="ts">
import product1 from '../assets/images/product1.png'
import product2 from '../assets/images/product2.png'
import product3 from '../assets/images/product3.png'
import product4 from '../assets/images/product4.png'

const products = [
  { name: 'SHR Beauty Machine', image: product1 },
  { name: 'E-Light / RF / Pico\nAll In One Machine', image: product2 },
  { name: 'SHR / SSR / Pico\nBeauty Machine', image: product3 },
  { name: 'SHR Beauty Machine', image: product4 },
]
</script>

<template>
  <section class="product-section">
    <div class="page-container">
      <div class="section-heading">
        <h2>PRODUCT CENTER</h2>
        <span class="heading-line" aria-hidden="true"></span>
      </div>

      <div class="product-grid">
        <article v-for="product in products" :key="product.name" class="product-card">
          <div class="product-image-wrap">
            <img :src="product.image" :alt="product.name.replace('\n', ' ')" />
          </div>
          <h3>{{ product.name }}</h3>
        </article>
      </div>

      <a class="product-button" href="#">All Product</a>
    </div>
  </section>
</template>
