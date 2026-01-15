<template>
  <div class="top-bar">
    <div class="container">
      <span>Öffnungszeiten: 08:00 - 20:00</span>
      <span>Tel: +49 (0) 123 456789</span>
      <span>Wetter: 22°C, Sonnig</span>
    </div>
  </div>
  <header id="main-header" :class="{ 'is-sticky': isSticky }">
    <div class="container header-content">
      <div class="logo">
        <span class="logo-text">Golfclub Sonnenhügel</span>
      </div>
      <nav>
        <ul>
          <li><a href="#anlage">Golfanlage</a></li>
          <li><a href="#gaeste">Gäste</a></li>
          <li><a href="#mitgliedchaft">Mitgliedschaft</a></li>
          <li><a href="#akademie">Akademie</a></li>
          <li><a href="#turniere">Turniere</a></li>
          <li><a href="#club">Club</a></li>
          <li><a href="#aktuelles">Aktuelles</a></li>
          <li><a href="#kontakt">Kontakt</a></li>
        </ul>
      </nav>
      <div class="header-ctas">
        <a href="#" class="btn btn-secondary">Mitglied werden</a>
        <a href="#" class="btn btn-primary">Startzeit buchen</a>
      </div>
    </div>
  </header>
</template>

<script setup>
import { ref, onMounted, onUnmounted } from 'vue';

const isSticky = ref(false);

const handleScroll = () => {
  isSticky.value = window.scrollY > 50;
};

onMounted(() => {
  window.addEventListener('scroll', handleScroll);
});

onUnmounted(() => {
  window.removeEventListener('scroll', handleScroll);
});
</script>

<style scoped>
/* Scoped styles are handled globally for this mockup to maintain consistency, 
   but we can add local adjustments here if needed. */
</style>
