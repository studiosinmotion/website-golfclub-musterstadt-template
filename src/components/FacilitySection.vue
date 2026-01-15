<template>
  <section class="facility section-padding" id="anlage">
    <div class="container">
      <h6 class="section-label">Entdecken</h6>
      <h2 class="section-title">Unsere Golfanlage</h2>
      <div class="card-grid">
        <div v-for="card in cards" :key="card.title" class="card">
          <div class="card-img" :style="{ backgroundImage: `url(${card.image})` }"></div>
          <div class="card-body">
            <h3>{{ card.title }}</h3>
            <p>{{ card.description }}</p>
            <a href="#" class="link-btn">Mehr erfahren</a>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
const cards = [
  { 
    title: 'Die Plätze', 
    description: 'Anspruchsvolles Design trifft auf atemberaubende Natur.',
    image: '/golf_hero_vibe_1768458200914.png'
  },
  { 
    title: 'Übungsanlagen', 
    description: 'Perfektionieren Sie Ihr Spiel auf unserer weitläufigen Range.',
    image: '/golf_training_academy_1768458233400.png'
  },
  { 
    title: 'Gastronomie', 
    description: 'Kulinarische Highlights mit Blick auf das 18. Grün.',
    image: '/golf_clubhouse_gastronomy_1768458218193.png'
  }
];
</script>
