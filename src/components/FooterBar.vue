<script setup lang="ts">
import { NAV_ITEMS } from '../constants/navigation'
import FacebookIcon from './icons/FacebookIcon.vue'
import GlobeIcon from './icons/GlobeIcon.vue'
import LinkedInIcon from './icons/LinkedInIcon.vue'
import PhoneIcon from './icons/PhoneIcon.vue'
import SearchGlobeIcon from './icons/SearchGlobeIcon.vue'
import TwitterIcon from './icons/TwitterIcon.vue'
import YoutubeIcon from './icons/YoutubeIcon.vue'

const contactItems = [
  { text: 'TEL.:+86 13810472608', icon: PhoneIcon },
  { text: 'Email:us@globalipl.com', icon: SearchGlobeIcon },
  { text: 'URL:www.globaliplaser.com', icon: GlobeIcon },
]

const socialLinks = [
  { label: 'Facebook', icon: FacebookIcon },
  { label: 'LinkedIn', icon: LinkedInIcon },
  { label: 'YouTube', icon: YoutubeIcon },
  { label: 'Twitter', icon: TwitterIcon },
]
</script>

<template>
  <footer class="footer-bar">
    <div class="footer-inner page-container">
      <nav class="footer-nav" aria-label="Footer navigation">
        <a v-for="item in NAV_ITEMS" :key="item" href="#">{{ item }}</a>
      </nav>

      <div class="footer-contact">
        <div v-for="item in contactItems" :key="item.text" class="contact-item">
          <component :is="item.icon" />
          <span>{{ item.text }}</span>
        </div>
      </div>

      <p class="footer-address">
        Headquarter Add.: floor 2 and 8, qunyinghui bldg, jinyuan rd 32, daxing economic
        development zone, beijing, china 102628
      </p>

      <div class="footer-socials" aria-label="Social links">
        <a v-for="link in socialLinks" :key="link.label" href="#" :aria-label="link.label">
          <component :is="link.icon" />
        </a>
      </div>
    </div>
  </footer>
</template>

<style scoped>
.footer-bar {
  background: var(--footer-bg);
  min-height: 280px;
  padding: 47px 0 36px;
  text-align: center;
}

.footer-nav {
  display: flex;
  align-items: center;
  justify-content: center;
  flex-wrap: wrap;
  gap: 0;
  margin: 0 0 37px;
  padding: 0;
  list-style: none;
}

.footer-nav a {
  display: inline-flex;
  align-items: center;
  color: var(--text-brown-black);
  font-family: Arial, Helvetica, sans-serif;
  font-size: 19.2px;
  font-weight: 400;
  line-height: 1;
}

.footer-nav a:not(:last-child)::after {
  content: "";
  width: 2px;
  height: 13px;
  margin: 0 31px;
  background: var(--line-dark);
}

.footer-contact {
  display: flex;
  justify-content: center;
  align-items: center;
  flex-wrap: wrap;
  gap: 32px;
  color: var(--text-black);
  font-family: Arial, Helvetica, sans-serif;
  font-size: 19px;
  font-weight: 400;
  line-height: 1;
  margin-bottom: 18px;
}

.contact-item {
  display: inline-flex;
  align-items: center;
  gap: 6px;
}

.contact-item :deep(.contact-icon) {
  width: var(--contact-icon-size);
  height: var(--contact-icon-size);
  display: block;
  object-fit: contain;
  flex: 0 0 var(--contact-icon-size);
  color: var(--text-black);
  fill: currentColor;
  stroke: currentColor;
}

.contact-item :deep(.globe-icon) {
  width: var(--contact-icon-size);
  height: var(--contact-icon-size);
  color: var(--icon-dark);
  flex-shrink: 0;
}

.footer-address {
  margin: 0 auto 31px;
  color: var(--text-black);
  font-size: 19px;
  line-height: 1.5;
}

.footer-socials {
  display: flex;
  justify-content: center;
  align-items: center;
  gap: 26px;
}

.footer-socials a {
  width: 34px;
  height: 34px;
  display: inline-flex;
  align-items: center;
  justify-content: center;
  border-radius: 50%;
  color: #ffffff;
  background: #6f6f6f;
  line-height: 1;
  transition:
    background-color 0.2s ease,
    transform 0.2s ease;
}

.footer-socials a:hover {
  background: var(--primary-purple);
  transform: translateY(-1px);
}

.footer-socials a :deep(svg) {
  width: 18px;
  height: 18px;
  display: block;
  fill: currentColor;
}

.footer-socials a[aria-label="Facebook"] :deep(svg) {
  transform: translateX(1px);
}

.footer-socials a[aria-label="YouTube"] :deep(svg) {
  width: 19px;
  height: 19px;
}

@media (max-width: 1200px) {
  .footer-nav a {
    font-size: 15px;
  }

  .footer-contact {
    font-size: 14px;
  }

  .footer-bar {
    min-height: 240px;
  }
}

@media (max-width: 768px) {
  .footer-nav a {
    font-size: 13px;
  }

  .footer-nav a:not(:last-child)::after {
    margin: 0 14px;
  }

  .footer-contact {
    gap: 12px 22px;
    font-size: 13px;
  }
}

@media (max-width: 560px) {
  .footer-nav {
    row-gap: 12px;
  }
}
</style>
