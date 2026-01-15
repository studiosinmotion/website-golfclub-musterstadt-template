<template>
  <footer>
    <div class="container footer-grid">
      <div class="footer-col">
        <h3>Kontakt</h3>
        <p>Sonnenhügel Allee 1</p>
        <p>12345 Golfstadt</p>
        <p>Deutschland</p>
        <p>E-Mail: info@golf-sonnenhuegel.de</p>
      </div>
      <div class="footer-col">
        <h3>Öffnungszeiten</h3>
        <p>Sommersaison: 07:00 - 21:00</p>
        <p>Wintersaison: 09:00 - 17:00</p>
        <p>Restaurant: 11:00 - 23:00</p>
      </div>
      <div class="footer-col">
        <h3>Schnellzugriff</h3>
        <ul>
          <li><a href="#">Platzstatus</a></li>
          <li><a href="#">Turnieranmeldung</a></li>
          <li><a href="#">Gäste-Info</a></li>
          <li><a href="#">Shop</a></li>
        </ul>
      </div>
      <div class="footer-col">
        <h3>Newsletter</h3>
        <p>Abonnieren Sie unseren Newsletter für aktuelle News.</p>
        <form class="newsletter-form" @submit.prevent>
          <input type="email" placeholder="E-Mail Adresse">
          <button type="submit" class="btn btn-primary">Anmelden</button>
        </form>
      </div>
    </div>
    <div class="container footer-bottom">
      <div class="legal-links">
        <a href="#">Impressum</a>
        <a href="#">Datenschutz</a>
        <a href="#">Barrierefreiheit</a>
      </div>
      <div class="socials">
        <a href="#">FB</a>
        <a href="#">IG</a>
        <a href="#">LI</a>
      </div>
      <p>&copy; 2026 Golfclub Sonnenhügel. Alle Rechte vorbehalten.</p>
    </div>
  </footer>
</template>
