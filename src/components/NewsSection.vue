<template>
  <section class="news section-padding" id="aktuelles">
    <div class="container">
      <div class="section-header">
        <div>
          <h6 class="section-label">Aktuelles</h6>
          <h2 class="section-title">Aus dem Club</h2>
        </div>
        <a href="#" class="btn btn-outline">Alle Beiträge</a>
      </div>
      <div class="news-grid">
        <div v-for="item in news" :key="item.title" class="news-item">
          <div class="news-img" :style="{ backgroundImage: `url(${item.image})` }"></div>
          <div class="news-content">
            <span class="date">{{ item.date }}</span>
            <h4>{{ item.title }}</h4>
            <p>{{ item.excerpt }}</p>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
const news = [
  {
    date: '15. Januar 2026',
    title: 'Rückblick: Der Neujahrsempfang',
    excerpt: 'Ein glanzvoller Abend voller Pläne für die kommende Saison...',
    image: '/golf_news_event_1768458247255.png'
  },
  {
    date: '12. Januar 2026',
    title: 'Platzpflege im Fokus',
    excerpt: 'Unser Greenkeeper-Team arbeitet an der perfekten Spielfläche...',
    image: '/golf_hero_vibe_1768458200914.png'
  },
  {
    date: '10. Januar 2026',
    title: 'Neuer Pro im Trainerteam',
    excerpt: 'Wir begrüßen Alexander Weber in unserer Golfakademie...',
    image: '/golf_news_event_1768458247255.png'
  }
];
</script>
