<template>
  <section class="service-desk container">
    <div class="service-tiles">
      <a v-for="tile in tiles" :key="tile.label" href="#" class="tile">
        <div class="tile-icon">{{ tile.icon }}</div>
        <span>{{ tile.label }}</span>
      </a>
    </div>
  </section>
</template>

<script setup>
const tiles = [
  { label: 'Turnierkalender', icon: '📅' },
  { label: 'Greenfee & Gäste', icon: '⛳' },
  { label: 'Training buchen', icon: '🎓' },
  { label: 'Platzreife', icon: '⭐' },
  { label: 'Kontakt & Anfahrt', icon: '📍' }
];
</script>
