<script setup lang="ts">
const navItems = ['HOME', 'PRODUCTS', 'ABOUT US', 'TREATMENT', 'SERVICE', 'NEWS', 'CONTACT US']
</script>

<template>
  <footer class="footer-bar">
    <div class="footer-inner page-container">
      <nav class="footer-nav" aria-label="Footer navigation">
        <a v-for="item in navItems" :key="item" href="#">{{ item }}</a>
      </nav>

      <div class="footer-contact">
        <div class="contact-item">
          <svg class="contact-icon" viewBox="0 0 24 24" aria-hidden="true">
            <path
              d="M5 5h14c1.1 0 2 .9 2 2v3.2h-5.1V8.7H8.1v1.5H3V7c0-1.1.9-2 2-2Zm1.2 6.8h11.6L21 15v5H3v-5l3.2-3.2ZM5 15.8V18h14v-2.2l-2.1-2H7.1L5 15.8ZM12 14.4a2.1 2.1 0 1 1 0 4.2 2.1 2.1 0 0 1 0-4.2Zm-7-6.2h1.4V7H5v1.2Zm12.6 0H19V7h-1.4v1.2Z"
            />
          </svg>
          <span>TEL.:+86 13810472608</span>
        </div>

        <div class="contact-item">
          <svg class="contact-icon" viewBox="0 0 24 24" aria-hidden="true">
            <path
              d="M10 3a7 7 0 0 1 6.9 8.2 5.5 5.5 0 0 0-1.7-.9V10h-3.1a12 12 0 0 1-.2 1.9 5.6 5.6 0 0 0-1.4 1.3c.3-.9.5-2 .5-3.2H9c.1 2 .5 3.7 1 4.8h.1A5.5 5.5 0 0 0 10 17a7 7 0 0 1 0-14Zm-5.8 8h3.7a13.9 13.9 0 0 1 0-2H4.2a5.4 5.4 0 0 0 0 2ZM5 7.5h3.1c.2-1 .4-1.8.8-2.5A5.1 5.1 0 0 0 5 7.5Zm0 5a5.1 5.1 0 0 0 3.9 2.5c-.4-.7-.6-1.5-.8-2.5H5ZM10 4.4c-.4.6-.8 1.7-1 3.1h2c-.2-1.4-.6-2.5-1-3.1Zm1.2 4.6H8.8a11.6 11.6 0 0 0 0 2h2.4a11.6 11.6 0 0 0 0-2Zm-.1-4c.4.7.6 1.5.8 2.5H15A5.1 5.1 0 0 0 11.1 5Zm6.4 7a3.5 3.5 0 0 1 2.8 5.7l2.3 2.3-1.6 1.6-2.3-2.3a3.5 3.5 0 1 1-1.2-7.3Zm0 2a1.5 1.5 0 1 0 0 3 1.5 1.5 0 0 0 0-3Z"
            />
          </svg>
          <span>Email:us@globalipl.com</span>
        </div>

        <div class="contact-item">
          <svg class="contact-icon" viewBox="0 0 24 24" aria-hidden="true">
            <path
              d="M12 3a9 9 0 1 0 0 18 9 9 0 0 0 0-18Zm6.8 8h-3.2a14.5 14.5 0 0 0-.9-4.4 7.1 7.1 0 0 1 4.1 4.4ZM12 5c.7 1 1.3 3 1.5 6h-3c.2-3 .8-5 1.5-6Zm-2.7 1.6a14.5 14.5 0 0 0-.9 4.4H5.2a7.1 7.1 0 0 1 4.1-4.4ZM5.2 13h3.2c.1 1.7.4 3.2.9 4.4A7.1 7.1 0 0 1 5.2 13Zm6.8 6c-.7-1-1.3-3-1.5-6h3c-.2 3-.8 5-1.5 6Zm1.5-8h-3c.1-2.3.6-4.1 1.5-5.4.9 1.3 1.4 3.1 1.5 5.4Zm1.2 6.4c.5-1.2.8-2.7.9-4.4h3.2a7.1 7.1 0 0 1-4.1 4.4Z"
            />
          </svg>
          <span>URL:www.globaliplaser.com</span>
        </div>
      </div>

      <p class="footer-address">
        Headquarter Add.: floor 2 and 8, qunyinghui bldg, jinyuan rd 32, daxing economic
        development zone, beijing, china 102628
      </p>

      <div class="footer-socials" aria-label="Social links">
        <a href="#" aria-label="Facebook">
          <svg viewBox="0 0 24 24" aria-hidden="true">
            <path
              d="M14.2 8.1h2.4V4.4c-.4-.1-1.8-.2-3.3-.2-3.3 0-5.5 2-5.5 5.6v3.1H4.2V17h3.6v7h4.4v-7h3.6l.6-4.1h-4.2V10.2c0-1.2.3-2.1 2-2.1Z"
            />
          </svg>
        </a>
        <a href="#" aria-label="LinkedIn">
          <svg viewBox="0 0 24 24" aria-hidden="true">
            <path
              d="M6.7 8.8H2.9V21h3.8V8.8ZM4.8 3C3.6 3 2.6 4 2.6 5.2s1 2.1 2.2 2.1S7 6.4 7 5.2 6 3 4.8 3Zm16.6 11.2c0-3.6-1.9-5.7-4.7-5.7-2.2 0-3.2 1.2-3.7 2V8.8H9.3V21h3.8v-6.1c0-1.6.3-3.2 2.3-3.2s2 1.9 2 3.3v6h3.9v-6.8Z"
            />
          </svg>
        </a>
        <a href="#" aria-label="YouTube">
          <svg viewBox="0 0 24 24" aria-hidden="true">
            <path
              d="M21.6 7.2c-.2-.9-.9-1.6-1.8-1.8C18.2 5 12 5 12 5s-6.2 0-7.8.4c-.9.2-1.6.9-1.8 1.8C2 8.8 2 12 2 12s0 3.2.4 4.8c.2.9.9 1.6 1.8 1.8 1.6.4 7.8.4 7.8.4s6.2 0 7.8-.4c.9-.2 1.6-.9 1.8-1.8.4-1.6.4-4.8.4-4.8s0-3.2-.4-4.8ZM10 15V9l5.2 3L10 15Z"
            />
          </svg>
        </a>
        <a href="#" aria-label="Twitter">
          <svg viewBox="0 0 24 24" aria-hidden="true">
            <path
              d="M21.8 6.2c-.7.3-1.4.5-2.2.6.8-.5 1.4-1.2 1.7-2.1-.7.4-1.6.8-2.4.9A3.8 3.8 0 0 0 12.3 9c0 .3 0 .6.1.9-3.2-.2-6-1.7-7.9-4-.3.6-.5 1.2-.5 1.9 0 1.3.7 2.5 1.7 3.2-.6 0-1.2-.2-1.7-.5 0 1.9 1.3 3.4 3.1 3.8-.3.1-.7.1-1 .1-.2 0-.5 0-.7-.1.5 1.6 1.9 2.7 3.6 2.7A7.7 7.7 0 0 1 3.3 19c1.7 1.1 3.7 1.7 5.9 1.7 7.1 0 11-5.9 11-11v-.5c.6-.9 1.2-1.8 1.6-3Z"
            />
          </svg>
        </a>
      </div>
    </div>
  </footer>
</template>
