<template>
  <section id="about" class="about-section">
    <div class="about-container">

      <!-- IMAGENS SOBREPOSTAS (coluna esquerda) -->
      <div class="about-image fade-slide">
        <div class="image-stack">
          <img src="@/assets/images/sobre/atividade_ongArcoiris.jpg" alt="Imagem 1" class="stack-img" />
          <img src="@/assets/images/sobre/equipe-OngArcoiris.jpg" alt="Imagem 2" class="stack-img" />
          <img src="@/assets/images/banner 2 - Ong.jpg" alt="Imagem 3" class="stack-img" />
        </div>
      </div>

      <!-- TEXTO (coluna direita) -->
      <div class="about-box fade-slide">
        <h2>Sobre a ONG</h2>
        <p>
          A Associação Arco-Íris é uma Organização Não Governamental (ONG) dedicada à transformação social no bairro Parque Residencial São Clemente. 
          Atuamos como um catalisador de mudança, promovendo ativamente atividades sociais, culturais e educacionais que beneficiam toda a comunidade.
          Nosso compromisso fundamental é fortalecer os vínculos comunitários, transformar realidades e criar oportunidades concretas para o desenvolvimento
          pleno de crianças, jovens e famílias da região.
        </p>
      </div>

    </div>
  </section>
</template>

<style scoped>
.about-section {
  width: 100%;
  padding: 80px 20px;
  display: flex;
  justify-content: center;
}

.about-container {
  max-width: 1300px;
  display: flex;
  align-items: center;
  gap: 180px;
}

/* --- IMAGEM SOBREPOSTA --- */
.about-image {
  position: relative;
  width: 650px;
  height: 650px;
}

.image-stack {
  position: relative;
  width: 100%;
  height: 100%;
}

.stack-img {
  width: 260px;
  height: 260px;
  border-radius: 50%;
  object-fit: cover;
  position: absolute;
  box-shadow: 0 8px 25px rgba(0,0,0,0.2);
  transition: transform 0.4s ease, box-shadow 0.4s ease;
}

.stack-img:nth-child(1) { top: 0; left: 0; z-index: 3; }
.stack-img:nth-child(2) { top: 100px; left: 220px; z-index: 2; }
.stack-img:nth-child(3) { top: 320px; left: 120px; z-index: 1; }

/* Efeito hover: imagens se movem */
.stack-img:hover {
  transform: translateY(-12px) scale(1.08);
  box-shadow: 0 15px 35px rgba(0,0,0,0.35);
}

/* --- TEXTO --- */
.about-box {
  max-width: 700px;
}

.about-box h2 {
  color: var(--secondary);
  font-size: 2.5rem;
  margin-bottom: 20px;
  font-weight: 700;
}

.about-box p {
  font-size: 1.25rem;
  color: var(--text);
  line-height: 1.7;
}

/* ---- ANIMAÇÃO DE ENTRADA ---- */
.fade-slide {
  opacity: 0;
  transform: translateY(30px);
  animation: fadeSlideIn 1s forwards;
}

.fade-slide:nth-child(1) { animation-delay: 0.3s; }
.fade-slide:nth-child(2) { animation-delay: 0.5s; }

@keyframes fadeSlideIn {
  to {
    opacity: 1;
    transform: translateY(0);
  }
}

/* ---- RESPONSIVO ---- */
@media (max-width: 900px) {
  .about-container {
    flex-direction: column;
    text-align: center;
    gap: 50px;
  }

  .about-image {
    width: 90%;
    height: auto;
    margin-bottom: 40px;
  }

  .stack-img {
    position: relative;
    top: auto;
    left: auto;
    margin: 0 -20px 0 0;
    width: 200px;
    height: 200px;
  }

  .about-box h2 {
    font-size: 2rem;
  }

  .about-box p {
    font-size: 1.1rem;
  }
}
</style>
