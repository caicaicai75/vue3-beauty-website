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
            Beijing Globalipl Development Co., Ltd. is one profession-al aesthetic machine Supplier in Beijing,
            China.Our
            company was built in 2003 and had 20 years experiences of exporting. Globalipl is engaged in development,
            research, sale and after sale of aesthetic machine. Our main business focuses on de-veloping of high quality
            aesthetic equipment, which created advanced position in this field.
          </p>
        </div>
      </article>

      <div class="about-model">
        <img :src="modelImg" alt="Beauty model" />
      </div>
    </div>
  </section>
</template>

<style scoped>
.about-section {
  background: #ffffff;
  height: 1008px;
  padding: 0;
  overflow: hidden;
}

.about-inner {
  width: min(var(--wide-page-width), 100%);
  height: 100%;
  position: relative;
}

.about-card {
  position: absolute;
  top: 160px;
  left: 248px;
  z-index: 2;
  width: 712px;
  height: 711px;
  min-height: 711px;
  margin-top: 0;
  padding: 20px;
  background-color: var(--primary-purple);
  background-size: cover;
  background-position: center;
}

.about-card-border {
  height: 100%;
  min-height: 671px;
  display: flex;
  flex-direction: column;
  justify-content: center;
  padding: 48px 58px 42px;
  border: 4px solid rgba(255, 255, 255, 0.92);
  color: #ffffff;
}

.about-title {
  margin: 0 0 34px;
  color: #ffffff;
  font-family: "BERNIERSHADE", Impact, "Arial Black", sans-serif;
  font-size: 38.29px;
  line-height: 1.25;
  letter-spacing: 4px;
  font-weight: 400;
  text-transform: uppercase;
  text-align: left;
  text-shadow:
    3px 3px 0 rgba(96, 78, 116, 0.75),
    0 0 1px rgba(255, 255, 255, 0.9);
}

.about-desc {
  width: 100%;
  max-width: 524px;
  margin: 28px auto 0;
  color: #ffffff;
  font-family: Arial, Helvetica, sans-serif;
  font-size: 19px;
  font-weight: 400;
  line-height: 1.75;
  text-align: left;
  text-indent: 2em;
}

.about-model {
  position: absolute;
  left: 698px;
  right: -110px;
  top: 0;
  bottom: 0;
  display: flex;
  align-items: flex-start;
  justify-content: flex-end;
  margin: 0;
}

.about-model img {
  width: 1126px;
  height: auto;
  object-fit: contain;
}

@media (max-width: 1200px) {
  .about-model {
    left: 46%;
    right: -8%;
    top: 20px;
  }

  .about-inner {
    width: min(100% - 52px, 1080px);
    height: 650px;
  }

  .about-section {
    height: 650px;
  }

  .about-card {
    top: 84px;
    left: 0;
    width: 470px;
    height: 445px;
    min-height: 445px;
    margin-top: 0;
    padding: 17px;
  }

  .about-card-border {
    min-height: 411px;
    padding: 36px 36px 34px;
  }

  .about-title {
    font-size: 27px;
  }

  .about-desc {
    max-width: 420px;
    font-size: 13px;
  }

  .about-model img {
    width: 650px;
  }
}

@media (max-width: 960px) {
  .about-inner {
    height: auto;
    display: flex;
    flex-direction: column;
    align-items: center;
    gap: 30px;
  }

  .about-section {
    height: auto;
    padding: 56px 0 30px;
  }

  .about-card {
    position: relative;
    top: auto;
    left: auto;
    width: min(470px, 100%);
  }

  .about-model {
    position: relative;
    inset: auto;
    display: block;
  }

  .about-model img {
    width: min(650px, 100%);
  }
}

@media (max-width: 768px) {
  .about-section {
    padding-top: 56px;
  }

  .about-card-border {
    padding: 28px 24px;
  }

  .about-title {
    font-size: 22px;
    margin-bottom: 26px;
  }

  .about-desc {
    width: 100%;
    font-size: 13px;
  }
}

@media (max-width: 560px) {
  .about-card {
    padding: 12px;
  }

  .about-card-border {
    min-height: auto;
    border-width: 3px;
  }
}
</style>
