<template>
  <section class="hero">
    <div class="hero-image" :style="{ backgroundImage: `url(${heroImage})` }"></div>
    <div class="hero-overlay"></div>
    <div class="container hero-content">
      <h1 class="fade-up">Willkommen im<br>Golfclub Sonnenhügel</h1>
      <p class="fade-up delay-1">Erleben Sie erstklassigen Golfsport in einer Atmosphäre von zeitloser Eleganz und Ruhe. Vor den Toren der Stadt erwartet Sie ein Ort der Begegnung und sportlichen Leidenschaft.</p>
      <div class="hero-actions fade-up delay-2">
        <a href="#" class="btn btn-primary btn-large">Startzeit buchen</a>
        <a href="#" class="btn btn-outline btn-large">Mitglied werden</a>
      </div>
    </div>

    <!-- STATUS BAR -->
    <div class="status-bar container">
      <div v-for="item in statusItems" :key="item.label" class="status-item">
        <span class="label">{{ item.label }}</span>
        <span class="value">{{ item.value }}</span>
      </div>
    </div>
  </section>
</template>

<script setup>
const heroImage = '/golf_hero_vibe_1768458200914.png';

const statusItems = [
  { label: 'Platzstatus', value: 'Platz offen' },
  { label: 'Range', value: 'Geöffnet' },
  { label: 'Carts', value: 'Erlaubt' },
  { label: 'Sekretariat', value: '08:00 - 18:00' }
];
</script>
