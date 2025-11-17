<template>
  <footer class="footer fade-in">
    <div class="footer-grid">

      <!-- COLUNA ESQUERDA -->
      <div class="col left-col">
        <div class="logo-row">
          <img
            src="@/assets/images/Logosemfundo.png"
            alt="Logo ONG Arco-Íris"
            class="logo-footer"
          />
          <h2 class="ong-name">ONG ARCO-ÍRIS</h2>
        </div>

        <p class="ong-desc">
          ONG ARCO-ÍRIS é uma organização não governamental que atende crianças,
          jovens e mulheres em vulnerabilidade social.
        </p>
      </div>

      <!-- COLUNA CENTRAL -->
      <div class="col">
        <h3 class="title">Nos Visite</h3>
        <p class="info">
          Rua São João Batista, 695<br />
          Parque Residencial São Clemente<br />
          13190-000 — Monte Mor, SP<br /><br />
          <strong>Contato:</strong> (19) 99429-6341
        </p>
      </div>

      <!-- COLUNA DIREITA – REDES SOCIAIS -->
      <div class="col social-column-container">
        <h3 class="title social-title">Redes Sociais</h3>

        <div class="social-column">
          <a class="social-link" href="https://www.instagram.com/ongarcoiris/" target="_blank">
            <img src="@/assets/images/icones/instagram.png" alt="Instagram" class="icon" />
          </a>

          <a class="social-link" href="https://www.facebook.com/ongarcoirisprojetos/?locale=pt_BR" target="_blank">
            <img src="@/assets/images/icones/facebook.png" alt="Facebook" class="icon" />
          </a>

          <a class="social-link" href="https://wa.me/19994296341" target="_blank">
            <img src="@/assets/images/icones/social.png" alt="WhatsApp" class="icon" />
          </a>
        </div>
      </div>

    </div>
  </footer>
</template>

<script setup lang="ts"></script>

<style scoped>
/* ---- FOOTER BASE ---- */
.footer {
  width: 100vw;
  background-color: #1d3557;
  color: white;
  padding: 40px 60px 18px 60px;

  border-top: 3px solid #457b9d;

  position: relative;
  left: 50%;
  margin-left: -50vw;
}

/* ---- GRID INTERNO ---- */
.footer-grid {
  width: 100%;
  display: grid;
  grid-template-columns: 1.2fr 1fr 0.8fr;
  gap: 90px;
}

/* ---- LOGO + NOME (CENTRALIZADOS) ---- */
.left-col {
  display: flex;
  flex-direction: column;
  align-items: center; /* Centraliza a coluna */
  text-align: center;
}

.logo-row {
  display: flex;
  align-items: center;
  justify-content: center; /* Centraliza horizontalmente */
  gap: 18px;
  margin-bottom: 14px;
}

.logo-footer {
  width: 58px;
  height: 58px;
  object-fit: contain;
}

/* ---- TEXTOS ---- */
.ong-name {
  font-size: 1.9rem;
  font-weight: 700;
}

.title {
  font-size: 1.4rem;
  font-weight: 600;
  margin-bottom: 18px;
}

.social-title {
  margin-bottom: 22px;
  text-align: left;
}

.ong-desc,
.info {
  color: #dce3e7;
  font-size: 1.05rem;
  line-height: 1.6;
}

/* ---- CONTAINER DA COLUNA DE ÍCONES ---- */
.social-column-container {
  display: flex;
  flex-direction: column;
  margin-left: 70px; /* distância apenas da coluna central */
}

/* ---- ÍCONES E LINKS ---- */
.social-column {
  display: flex;
  flex-direction: row;
  align-items: center;
  gap: 26px; /* espaçamento ENTRE ícones */
}

.social-link {
  display: flex;
  align-items: center;
  justify-content: center;
}

.icon {
  width: 34px;
  height: 34px;
  object-fit: contain;
  transition: 0.3s;
}

.icon:hover {
  transform: scale(1.13);
  filter: brightness(1.2);
}

/* ---- ANIMAÇÃO ---- */
.fade-in {
  animation: fadeIn 0.9s ease-in-out;
}

@keyframes fadeIn {
  from { opacity: 0; transform: translateY(10px); }
  to   { opacity: 1; transform: translateY(0); }
}

/* ---- RESPONSIVIDADE ---- */
@media (max-width: 900px) {
  .footer-grid {
    grid-template-columns: 1fr;
    gap: 40px;
  }

  .footer {
    padding: 40px 30px 10px 30px;
  }

  .social-column-container {
    margin-left: 0;
    align-items: center;
  }

  .logo-row {
    justify-content: center;
  }

  .left-col {
    text-align: center;
    align-items: center;
  }
}
</style>
