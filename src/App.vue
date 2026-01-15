<template>
  <div class="app-wrapper">
    <AppHeader />
    <main>
      <AppHero />
      <ServiceSection />
      <FacilitySection />
      <AcademySection />
      <NewsSection />
      <GallerySection />
      <TrustSection />
    </main>
    <AppFooter />
  </div>
</template>

<script setup>
import AppHeader from './components/AppHeader.vue';
import AppHero from './components/AppHero.vue';
import ServiceSection from './components/ServiceSection.vue';
import FacilitySection from './components/FacilitySection.vue';
import AcademySection from './components/AcademySection.vue';
import NewsSection from './components/NewsSection.vue';
import GallerySection from './components/GallerySection.vue';
import TrustSection from './components/TrustSection.vue';
import AppFooter from './components/AppFooter.vue';

import './assets/style.css';
</script>

<style>
/* Global styles are loaded from assets/style.css */
</style>
