<script setup lang="ts">
import logoImg from '../assets/images/logo.png'
import mapIcon from '../assets/images/map.png'
import searchIcon from '../assets/images/search.png'
import telIcon from '../assets/images/tel.png'

const navItems = ['HOME', 'PRODUCTS', 'ABOUT US', 'TREATMENT', 'SERVICE', 'NEWS', 'CONTACT US']
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
        <li v-for="item in navItems" :key="item" class="header-nav-item">
          <a href="#">{{ item }}</a>
        </li>
      </ul>
    </nav>
  </header>
</template>
