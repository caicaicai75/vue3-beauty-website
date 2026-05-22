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

<style scoped>
.product-section {
  height: 880px;
  padding: 58px 0 90px;
  background: #ffffff;
  text-align: center;
}

.section-heading h2 {
  margin: 0;
  color: var(--title-purple);
  font-family: Arial, Helvetica, sans-serif;
  font-size: 50px;
  line-height: 1.1;
  font-weight: 700;
}

.heading-line {
  position: relative;
  display: block;
  width: 193px;
  height: 1px;
  margin: 20px auto 71px;
  background: #67556f;
}

.heading-line::after {
  content: "";
  position: absolute;
  top: 50%;
  left: 50%;
  width: 8px;
  height: 8px;
  border: 1px solid #67556f;
  border-radius: 50%;
  background: #ffffff;
  transform: translate(-50%, -50%);
}

.product-grid {
  display: grid;
  grid-template-columns: repeat(4, 1fr);
  gap: 92px;
  align-items: start;
  max-width: 1130px;
  margin: 0 auto;
}

.product-card {
  display: flex;
  flex-direction: column;
  align-items: center;
  text-align: center;
}

.product-image-wrap {
  position: relative;
  width: 100%;
  height: 320px;
  display: flex;
  align-items: flex-end;
  justify-content: center;
  padding-bottom: 28px;
}

.product-image-wrap::after {
  content: "";
  position: absolute;
  left: 50%;
  bottom: 8px;
  width: 120px;
  height: 18px;
  border-radius: 50%;
  background: rgba(0, 0, 0, 0.12);
  filter: blur(4px);
  transform: translateX(-50%);
  z-index: 1;
}

.product-image-wrap img {
  position: relative;
  z-index: 2;
  max-width: 100%;
  max-height: 260px;
  object-fit: contain;
}

.product-card h3 {
  min-height: 56px;
  margin: 18px 0 0;
  color: #595757;
  font-family: Arial, Helvetica, sans-serif;
  font-size: 22px;
  line-height: 1.25;
  font-weight: 400;
  white-space: pre-line;
}

.product-button {
  width: 152.5px;
  height: 43.5px;
  min-height: 28px;
  display: inline-flex;
  align-items: center;
  justify-content: center;
  margin-top: 57px;
  padding: 0 12px;
  border: 1px solid var(--brand-purple);
  color: var(--brand-purple);
  font-family: Arial, Helvetica, sans-serif;
  font-size: 25.1px;
  font-weight: 400;
  line-height: 1;
  background: transparent;
  transition:
    color 0.2s ease,
    border-color 0.2s ease,
    background-color 0.2s ease;
}

.product-button:hover {
  border-color: var(--primary-purple);
  color: #ffffff;
  background: var(--primary-purple);
}

@media (max-width: 1200px) {
  .section-heading h2 {
    font-size: 36px;
  }

  .product-card h3 {
    font-size: 16px;
  }

  .product-button {
    font-size: 18px;
  }

  .product-section {
    height: auto;
    min-height: 720px;
    padding-top: 46px;
  }

  .product-grid {
    gap: 58px;
    max-width: 865px;
  }

  .product-image-wrap {
    height: 300px;
  }

  .product-image-wrap img {
    max-width: 100%;
    max-height: 250px;
  }
}

@media (max-width: 960px) {
  .product-grid {
    grid-template-columns: repeat(2, minmax(0, 1fr));
    max-width: 560px;
    gap: 36px 60px;
  }
}

@media (max-width: 768px) {
  .section-heading h2 {
    font-size: 28px;
  }

  .product-card h3 {
    font-size: 15px;
  }

  .product-button {
    font-size: 16px;
  }
}

@media (max-width: 560px) {
  .product-grid {
    grid-template-columns: 1fr;
    gap: 28px;
  }

  .product-image-wrap {
    height: 260px;
  }

  .product-image-wrap img {
    max-height: 220px;
  }
}
</style>
