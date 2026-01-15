<template>
  <div class="top-bar">
    <div class="container">
      <span>Öffnungszeiten: 08:00 - 20:00</span>
      <span>Tel: +49 (0) 123 456789</span>
      <span class="hidden-mobile">Wetter: 22°C, Sonnig</span>
    </div>
  </div>
  <header id="main-header" :class="{ 'is-sticky': isSticky, 'menu-open': isMenuOpen }">
    <div class="container header-content">
      <div class="logo">
        <span class="logo-text">Golfclub Sonnenhügel</span>
      </div>
      
      <!-- DESKTOP NAV -->
      <nav class="desktop-nav">
        <ul>
          <li v-for="item in navItems" :key="item.href">
            <a :href="item.href">{{ item.label }}</a>
          </li>
        </ul>
      </nav>

      <div class="header-ctas desktop-only">
        <a href="#" class="btn btn-secondary">Mitglied werden</a>
        <a href="#" class="btn btn-primary">Startzeit buchen</a>
      </div>

      <!-- MOBILE BURGER TOOL -->
      <button class="burger-menu" @click="toggleMenu" aria-label="Menu">
        <span class="burger-line"></span>
        <span class="burger-line"></span>
        <span class="burger-line"></span>
      </button>
    </div>

    <!-- MOBILE OVERLAY -->
    <transition name="fade">
      <div v-if="isMenuOpen" class="mobile-overlay">
        <nav class="mobile-nav">
          <ul>
            <li v-for="item in navItems" :key="item.href" @click="closeMenu">
              <a :href="item.href">{{ item.label }}</a>
            </li>
          </ul>
          <div class="mobile-ctas">
            <a href="#" class="btn btn-primary">Startzeit buchen</a>
            <a href="#" class="btn btn-secondary">Mitglied werden</a>
          </div>
        </nav>
      </div>
    </transition>
  </header>
</template>

<script setup>
import { ref, onMounted, onUnmounted } from 'vue';

const isSticky = ref(false);
const isMenuOpen = ref(false);

const navItems = [
  { label: 'Golfanlage', href: '#anlage' },
  { label: 'Gäste', href: '#gaeste' },
  { label: 'Mitgliedschaft', href: '#mitgliedchaft' },
  { label: 'Akademie', href: '#akademie' },
  { label: 'Turniere', href: '#turniere' },
  { label: 'Club', href: '#club' },
  { label: 'Aktuelles', href: '#aktuelles' },
  { label: 'Kontakt', href: '#kontakt' },
];

const toggleMenu = () => {
  isMenuOpen.value = !isMenuOpen.value;
  if (isMenuOpen.value) {
    document.body.style.overflow = 'hidden';
  } else {
    document.body.style.overflow = '';
  }
};

const closeMenu = () => {
  isMenuOpen.value = false;
  document.body.style.overflow = '';
};

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
.burger-menu {
  display: none;
  background: none;
  border: none;
  cursor: pointer;
  flex-direction: column;
  gap: 6px;
  padding: 10px;
  z-index: 2000;
}

.burger-line {
    width: 25px;
    height: 2px;
    background-color: var(--primary);
    transition: all 0.3s ease;
}

.menu-open .burger-line:nth-child(1) { transform: translateY(8px) rotate(45deg); }
.menu-open .burger-line:nth-child(2) { opacity: 0; }
.menu-open .burger-line:nth-child(3) { transform: translateY(-8px) rotate(-45deg); }

.mobile-overlay {
    position: fixed;
    top: 0;
    left: 0;
    width: 100%;
    height: 100vh;
    background: var(--white);
    z-index: 1500;
    display: flex;
    align-items: center;
    justify-content: center;
}

.mobile-nav ul {
    list-style: none;
    text-align: center;
    padding: 0;
}

.mobile-nav ul li {
    margin-bottom: 1.5rem;
}

.mobile-nav ul li a {
    display: block;
    font-size: 1.8rem;
    font-family: var(--font-serif);
    color: var(--primary) !important;
    visibility: visible;
}

.mobile-ctas {
    display: flex;
    flex-direction: column;
    gap: 1rem;
    margin-top: 3rem;
    align-items: center;
}

.fade-enter-active, .fade-leave-active { transition: opacity 0.3s ease; }
.fade-enter-from, .fade-leave-to { opacity: 0; }

@media (max-width: 768px) {
    .desktop-nav, .desktop-only {
        display: none;
    }
    .burger-menu {
        display: flex;
    }
    .hidden-mobile {
        display: none;
    }
}
</style>
