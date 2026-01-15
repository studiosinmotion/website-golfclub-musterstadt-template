<template>
  <section class="trust-strip">
    <div class="container">
      <div class="partners">
        <span v-for="p in partners" :key="p" class="partner">{{ p }}</span>
      </div>
      <blockquote class="testimonial">
        "Ein Ort, an dem man die Welt um sich herum vergisst. Exzellenter Service und ein traumhafter Platz."
        <cite>— Marc Steiner, Mitglied</cite>
      </blockquote>
    </div>
  </section>
</template>

<script setup>
const partners = ['PARTNER A', 'PARTNER B', 'PARTNER C', 'PARTNER D'];
</script>
