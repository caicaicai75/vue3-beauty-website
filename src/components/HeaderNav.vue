<script setup lang="ts">
import logoImg from '../assets/images/logo.png'
import mapIcon from '../assets/images/map.png'
import searchIcon from '../assets/images/search.png'
import telIcon from '../assets/images/tel.png'
import { NAV_ITEMS } from '../constants/navigation'
</script>

<template>
  <header class="site-header">
    <div class="header-top page-container">
      <a class="header-logo" href="#" aria-label="Globalipl home">
        <img :src="logoImg" alt="Globalipl" />
      </a>

      <div class="header-info">
        <span class="header-info-item">
          <img :src="telIcon" alt="" />
          Phone:+86 - xxxx xxxx
        </span>
        <span class="header-info-item">
          <img :src="mapIcon" alt="" />
          https://www.globaliplaser.com
        </span>
      </div>

      <label class="header-search" aria-label="Search">
        <img :src="searchIcon" alt="" />
        <input type="search" />
      </label>
    </div>

    <nav class="header-nav" aria-label="Primary navigation">
      <ul class="header-nav-list">
        <li v-for="item in NAV_ITEMS" :key="item" class="header-nav-item">
          <a href="#">{{ item }}</a>
        </li>
      </ul>
    </nav>
  </header>
</template>

<style scoped>
.site-header {
  background: #ffffff;
}

.header-top {
  height: 118px;
  min-height: 118px;
  display: grid;
  grid-template-columns: 300px 1fr 205px;
  align-items: center;
  gap: 34px;
}

.header-logo {
  justify-self: center;
}

.header-logo img {
  width: 130px;
  height: auto;
}

.header-info {
  display: flex;
  justify-content: flex-end;
  align-items: center;
  gap: 32px;
  color: #2c2932;
  font-size: 14px;
  white-space: nowrap;
}

.header-info-item {
  display: inline-flex;
  align-items: center;
  gap: 8px;
  color: var(--text-black);
  font-size: 19px;
}

.header-info-item img {
  width: 24px;
  height: 20px;
  object-fit: contain;
}

.header-search {
  width: 206px;
  height: 34px;
  display: flex;
  align-items: center;
  gap: 8px;
  padding: 0 14px;
  border: 1px solid #d8d6dc;
  border-radius: 999px;
  background: #ffffff;
}

.header-search img {
  width: 16px;
  height: 18px;
  opacity: 1;
}

.header-search input {
  min-width: 0;
  width: 100%;
  border: 0;
  outline: 0;
  color: var(--text-dark);
  background: transparent;
}

.header-nav {
  height: 86px;
  min-height: 86px;
  display: flex;
  align-items: center;
  justify-content: center;
  background: var(--hero-bg);
}

.header-nav-list {
  display: flex;
  align-items: center;
  justify-content: center;
  flex-wrap: wrap;
  gap: 0;
  margin: 0;
  padding: 0;
  list-style: none;
}

.header-nav-item {
  display: inline-flex;
  align-items: center;
  color: var(--text-brown-black);
  font-family: Arial, Helvetica, sans-serif;
  font-size: 19.2px;
  font-weight: 400;
  line-height: 1;
}

.header-nav-item:not(:last-child)::after {
  content: "";
  width: 2px;
  height: 13px;
  margin: 0 31px;
  background: var(--line-dark);
}

@media (max-width: 1200px) {
  .header-top {
    height: 86px;
    min-height: 86px;
    grid-template-columns: 190px 1fr 185px;
    gap: 20px;
  }

  .header-logo img {
    width: 104px;
  }

  .header-nav {
    height: 64px;
    min-height: 64px;
  }

  .header-nav-item {
    font-size: 15px;
  }

  .header-info {
    gap: 20px;
    font-size: 13px;
  }

  .header-search {
    width: 185px;
  }
}

@media (max-width: 960px) {
  .header-top {
    grid-template-columns: 140px 1fr;
  }

  .header-info {
    justify-content: flex-end;
    gap: 18px;
  }

  .header-search {
    grid-column: 1 / -1;
    justify-self: center;
    margin-bottom: 14px;
  }
}

@media (max-width: 768px) {
  .header-top {
    grid-template-columns: 1fr;
    gap: 12px;
    padding: 18px 0 14px;
    text-align: center;
  }

  .header-logo {
    justify-self: center;
  }

  .header-info {
    justify-content: center;
    flex-wrap: wrap;
  }

  .header-search {
    grid-column: auto;
    margin-bottom: 0;
  }

  .header-nav {
    padding: 14px 0;
  }

  .header-nav-list {
    padding: 0 14px;
    row-gap: 12px;
  }

  .header-nav-item {
    font-size: 13px;
  }

  .header-nav-item:not(:last-child)::after {
    margin: 0 14px;
  }
}
</style>
