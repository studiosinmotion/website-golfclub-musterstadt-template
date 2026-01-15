<template>
  <section class="gallery-slider section-padding bg-dark">
    <div class="container text-center">
      <h6 class="section-label light">Impressionen</h6>
      <h2 class="section-title light">Eindrücke vom Club</h2>
      <div class="horizontal-scroll">
        <div v-for="(img, index) in images" :key="index" class="gallery-item">
          <img :src="img" alt="Gallery Image">
        </div>
      </div>
      <div class="gallery-actions">
        <a href="#" class="btn btn-outline light">Zur Galerie</a>
      </div>
    </div>
  </section>
</template>

<script setup>
const images = [
  '/golf_hero_vibe_1768458200914.png',
  '/golf_clubhouse_gastronomy_1768458218193.png',
  '/golf_training_academy_1768458233400.png',
  '/golf_news_event_1768458247255.png',
  '/golf_hero_vibe_1768458200914.png'
];
</script>
