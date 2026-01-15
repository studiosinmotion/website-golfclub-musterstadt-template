<template>
  <section class="service-desk container">
    <div class="service-tiles">
      <a v-for="tile in tiles" :key="tile.label" href="#" class="tile">
        <div class="tile-icon" v-html="tile.icon"></div>
        <span>{{ tile.label }}</span>
      </a>
    </div>
  </section>
</template>

<script setup>
const tiles = [
  { 
    label: 'Turnierkalender', 
    icon: `<svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1" stroke-linecap="round" stroke-linejoin="round"><rect x="3" y="4" width="18" height="18" rx="2" ry="2"></rect><line x1="16" y1="2" x2="16" y2="6"></line><line x1="8" y1="2" x2="8" y2="6"></line><line x1="3" y1="10" x2="21" y2="10"></line></svg>` 
  },
  { 
    label: 'Greenfee & Gäste', 
    icon: `<svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1" stroke-linecap="round" stroke-linejoin="round"><path d="M4 22V4c0-1.1.9-2 2-2h12l4 4-4 4H6"></path><circle cx="12" cy="18" r="2"></circle></svg>` 
  },
  { 
    label: 'Training buchen', 
    icon: `<svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1" stroke-linecap="round" stroke-linejoin="round"><circle cx="12" cy="8" r="5"></circle><path d="M12 13v8"></path><path d="M9 21h6"></path></svg>` 
  },
  { 
    label: 'Platzreife', 
    icon: `<svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1" stroke-linecap="round" stroke-linejoin="round"><polygon points="12 2 15.09 8.26 22 9.27 17 14.14 18.18 21.02 12 17.77 5.82 21.02 7 14.14 2 9.27 8.91 8.26 12 2"></polygon></svg>` 
  },
  { 
    label: 'Kontakt & Anfahrt', 
    icon: `<svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="1" stroke-linecap="round" stroke-linejoin="round"><path d="M21 10c0 7-9 13-9 13s-9-6-9-13a9 9 0 0 1 18 0z"></path><circle cx="12" cy="10" r="3"></circle></svg>` 
  }
];
</script>

<style scoped>
.tile-icon :deep(svg) {
  width: 40px;
  height: 40px;
  color: var(--accent);
  transition: color 0.3s ease;
}

.tile:hover .tile-icon :deep(svg) {
  color: var(--white);
}
</style>
