<template>
  <section id="activities" class="activities-section">
    <div class="container">
      <h2>Conheça as nossas Atividades</h2>

      <div class="cards">
        <!-- Card 1 -->
        <div class="card">
          <img src="@/assets/images/atividades/Mercado do bem.jpg" alt="Reforço Escolar" class="card-img"/>
          <h3>Mercado do Bem </h3>
          <p>O Mercado do Bem do fundo social de Monte Mor é uma parceria com o Recicla Consimares.</p>
        </div>

        <!-- Card 2 -->
        <div class="card">
          <img src="@/assets/images/atividades/arrecadacao.jpg" alt="Artesanato" class="card-img"/>
          <h3>Arrecadação de mantimentos </h3>
          <p>Realizada no dia 11 de outubro, foram entregues 50 cestas básicas para famílias em situação vulnerável.</p>
        </div>

        <!-- Card 3 -->
        <div class="card">
          <img src="@/assets/images/atividades/DiaCrianSolidaria.jpg" alt="Música e Cultura" class="card-img"/>
          <h3>Dia das Crianças Solidário</h3>
          <p>Evento para comemorar o Dia das Crianças com brincadeiras, presentes, atividades, pintura de rostos e comidas.</p>
        </div>

        <!-- Card 4 -->
        <div class="card">
          <img src="@/assets/images/atividades/Natal.jpg" alt="Esporte" class="card-img"/>
          <h3>Natal Feliz</h3>
          <p>Festa do Natal Solidário com distribuição de presentes, fotos com o Papai Noel, atividades e comidas.</p>
        </div>

        <!-- Card 5 -->
        <div class="card">
          <img src="@/assets/images/atividades/Arrecadacao2.jpg" alt="Apoio Psicossocial" class="card-img"/>
          <h3>Doações para as vítimas de São Sebastião</h3>
          <p>Doações para as vítimas de São Sebastião.</p>
        </div>

        <!-- Card 6 -->
        <div class="card">
          <img src="@/assets/images/atividades/hamburgada.jpg" alt="Eventos Comunitários" class="card-img"/>
          <h3>Hamburgada do Bem</h3>
          <p>Segunda edição da Hamburgada do Bem, realizada para os moradores da comunidade.</p>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup lang="ts"></script>

<style scoped>
.activities-section {
  padding: 80px 20px;
  background-color: var(--light-bg);
  text-align: center;
}

.container {
  max-width: 1300px;
  margin: 0 auto;
}

h2 {
  font-size: 2.5rem;
  color: var(--secondary);
  margin-bottom: 50px;
  font-weight: 700;
}

.cards {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 40px;
  justify-items: center;
}

.card {
  background: #ffffff;
  border-radius: 12px;
  width: 100%;
  max-width: 300px; /* card maior */
  padding: 0; /* remover padding para imagem ocupar tudo */
  text-align: left;
  box-shadow: 0 8px 25px rgba(0,0,0,0.15);
  transition: transform 0.3s ease, box-shadow 0.3s ease;
  overflow: hidden; /* garante que nada vaze do card */
}

.card:hover {
  transform: translateY(-8px);
  box-shadow: 0 15px 35px rgba(0,0,0,0.25);
}

.card-img {
  width: 100%;
  height: 220px; /* maior para não cortar */
  object-fit: cover;
  margin-bottom: 15px;
  border-radius: 0; /* remove bordas */
}

.card h3 {
  font-size: 1.4rem;
  margin: 15px;
  margin-bottom: 10px;
  color: var(--secondary);
}

.card p {
  font-size: 0.95rem; /* fonte menor */
  color: var(--text);
  line-height: 1.5;
  margin: 0 15px 15px 15px;
}

/* RESPONSIVO */
@media (max-width: 1024px) {
  .cards {
    grid-template-columns: repeat(2, 1fr);
  }
}

@media (max-width: 680px) {
  .cards {
    grid-template-columns: 1fr;
  }

  .card-img {
    height: 200px;
  }
}
</style>
