<template>
  <section id="contact" class="contact-section">
    <div class="contact-container">

      <!-- COLUNA DE INFORMAÇÕES -->
      <div class="contact-info">
        <h2>Contato</h2>

        <div class="info-item">
          <span class="material-icons">email</span>
          <p>contato@arcoiris.org</p>
        </div>

        <div class="info-item">
          <span class="material-icons">phone</span>
          <p>(19) 99999-9999</p>
        </div>

        <div class="info-item">
          <span class="material-icons">location_on</span>
          <p>Parque Residencial São Clemente, Monte Mor</p>
        </div>
      </div>

      <!-- COLUNA DE MAPA -->
      <div class="contact-map">
        <iframe
          src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d3665.961582172685!2d-47.39855358452533!3d-22.882191385009536!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x94c8cc44e2d2b6ef%3A0x2f6f2efb8a1f7de4!2sParque%20Residencial%20S%C3%A3o%20Clemente%2C%20Monte%20Mor%20-%20SP!5e0!3m2!1spt-BR!2sbr!4v1699983057832!5m2!1spt-BR!2sbr"
          width="100%"
          height="300"
          style="border:0;"
          allowfullscreen=""
          loading="lazy"
          referrerpolicy="no-referrer-when-downgrade">
        </iframe>
      </div>

    </div>
  </section>
</template>

<script setup lang="ts"></script>

<style scoped>
@import url('https://fonts.googleapis.com/icon?family=Material+Icons');

.contact-section {
  padding: 80px 20px;
  background-color: var(--light-bg);
}

.contact-container {
  max-width: 1200px;
  margin: 0 auto;
  display: flex;
  gap: 60px;
  align-items: flex-start;
}

/* ---- COLUNA DE INFORMAÇÕES ---- */
.contact-info {
  flex: 1;
}

.contact-info h2 {
  font-size: 2.5rem;
  color: var(--secondary);
  margin-bottom: 30px;
  font-weight: 700;
}

.info-item {
  display: flex;
  align-items: center;
  margin-bottom: 20px;
}

.info-item span.material-icons {
  font-size: 2rem;
  color: var(--secondary);
  margin-right: 15px;
}

.info-item p {
  font-size: 1.15rem;
  color: var(--text);
  margin: 0;
}

/* ---- COLUNA DE MAPA ---- */
.contact-map {
  flex: 1;
  border-radius: 12px;
  overflow: hidden;
  box-shadow: 0 8px 25px rgba(0,0,0,0.15);
}

/* ---- RESPONSIVO ---- */
@media (max-width: 900px) {
  .contact-container {
    flex-direction: column;
  }

  .contact-map {
    width: 100%;
    height: 300px;
    margin-top: 30px;
  }
}
</style>
