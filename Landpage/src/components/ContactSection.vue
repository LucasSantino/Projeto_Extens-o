<template>
  <section id="contact" class="contact-section">
    <div class="contact-container">

      <!-- COLUNA DE INFORMAÇÕES -->
      <div class="contact-info">
        <h2>Contato</h2>
        <div class="info-item">
          <span class="material-icons">email</span>
          <p>ongarcoirisprojetos@gmail.com</p>
        </div>
        <div class="info-item">
          <span class="material-icons">phone</span>
          <p>(19) 99429-6341</p>
        </div>
        <div class="info-item">
  <span class="material-icons">location_on</span>
  <p class="address-text">
    Rua São João Batista, 695<br />
    Parque Residencial São Clemente – Monte Mor, SP
  </p>
</div>

      </div>

      <!-- COLUNA DO MAPA -->
      <div class="contact-map">
        <iframe
          src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d3687.0000000000005!2d-47.233333333333334!3d-22.932510000000003!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x94c8cc44e2d2b6ef%3A0x0!2sR.%20S%C3%A3o%20Jo%C3%A3o%20Batista%2C%20695%20-%20Parque%20Residencial%20S%C3%A3o%20Clemente%2C%20Monte%20Mor%20-%20SP%2C%2013197-236%2C%20Brasil!5e0!3m2!1spt-BR!2sbr!4v1700000000000"
          width="100%"
          height="350"
          style="border:0;"
          :allowfullscreen="true"
          loading="lazy"
          referrerpolicy="no-referrer-when-downgrade"
        ></iframe>
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
  flex-wrap: wrap;
}

.contact-info {
  flex: 1;
  min-width: 280px;
}

.contact-info h2 {
  font-size: 2.5rem;
  color: var(--secondary);
  margin-bottom: 30px;
  font-weight: 700;
}

.info-item {
  display: flex;
  align-items: flex-start;
  gap: 15px;
  margin-bottom: 20px;
}

.material-icons {
  font-size: 2rem;
  color: var(--secondary);
}

.info-item p {
  margin: 0;
  color: var(--text);
  font-size: 1.15rem;
  text-align: left; 
  line-height: 1.4;
}


.contact-map {
  flex: 1;
  min-width: 300px;
  border-radius: 12px;
  overflow: hidden;
  box-shadow: 0 8px 25px rgba(0,0,0,0.15);
}

@media (max-width: 900px) {
  .contact-container {
    flex-direction: column;
    align-items: center;
  }
}
</style>
