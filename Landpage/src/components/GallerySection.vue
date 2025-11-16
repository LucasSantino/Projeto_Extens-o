<template>
  <section id="gallery" class="gallery-section">
    <div class="gallery-container">
      <h2>Galeria de Imagens</h2>

      <div class="grid">
        <div class="img-box" v-for="(img, index) in currentImages" :key="index">
          <img :src="img" alt="Galeria ONG" />
        </div>
      </div>

      <div class="btn-group" v-if="images.length > imagesPerPage">
        <button class="btn-nav" @click="prevPage" :disabled="currentPage === 1">Anterior</button>
        <button class="btn-nav" @click="nextPage" :disabled="currentPage === totalPages">Próximo</button>
      </div>
    </div>
  </section>
</template>

<script setup lang="ts">
import { ref, computed } from 'vue';

// Todas as imagens do projeto
const images = [
  new URL('@/assets/images/sobre/atividade_ongArcoiris.jpg', import.meta.url).href,
  new URL('@/assets/images/sobre/equipe-OngArcoiris.jpg', import.meta.url).href,
  new URL('@/assets/images/banner 2 - Ong.jpg', import.meta.url).href,
  new URL('@/assets/images/atividades/Mercado do bem.jpg', import.meta.url).href,
  new URL('@/assets/images/atividades/arrecadacao.jpg', import.meta.url).href,
  new URL('@/assets/images/atividades/DiaCrianSolidaria.jpg', import.meta.url).href,
  new URL('@/assets/images/atividades/Natal.jpg', import.meta.url).href,
  new URL('@/assets/images/atividades/Arrecadacao2.jpg', import.meta.url).href,
  new URL('@/assets/images/atividades/evento.jpg', import.meta.url).href,
  new URL('@/assets/images/atividades/hamburgada.jpg', import.meta.url).href
];

const imagesPerPage = 9; // imagens por página
const currentPage = ref(1);

const totalPages = Math.ceil(images.length / imagesPerPage);

const currentImages = computed(() => {
  const start = (currentPage.value - 1) * imagesPerPage;
  return images.slice(start, start + imagesPerPage);
});

const nextPage = () => {
  if (currentPage.value < totalPages) currentPage.value++;
};

const prevPage = () => {
  if (currentPage.value > 1) currentPage.value--;
};
</script>

<style scoped>
.gallery-section {
  padding: 80px 20px;
  background-color: var(--light-bg);
  text-align: center;
}

.gallery-container {
  max-width: 1300px;
  margin: 0 auto;
}

h2 {
  font-size: 2.5rem;
  color: var(--secondary);
  margin-bottom: 30px;
  font-weight: 700;
}

/* GRID estilo celular */
.grid {
  display: grid;
  grid-template-columns: repeat(3, 1fr); /* 3 colunas */
  gap: 5px; /* imagens bem próximas */
}

.img-box img {
  width: 100%;
  aspect-ratio: 1; /* garante quadrado igual celular */
  object-fit: cover;
  border-radius: 20px; /* leve borda arredondada */
  transition: transform 0.3s ease;
}


.img-box img:hover {
  transform: scale(1.05);
}

/* BOTOES PAGINAÇÃO */
.btn-group {
  margin-top: 20px;
  display: flex;
  justify-content: center;
  gap: 15px;
}

.btn-nav {
  padding: 10px 25px;
  background-color: var(--secondary);
  color: #fff;
  border: none;
  border-radius: 6px;
  font-size: 1rem;
  cursor: pointer;
  transition: 0.3s;
}

.btn-nav:hover:not(:disabled) {
  background-color: #1d3557;
}

.btn-nav:disabled {
  background-color: #aaa;
  cursor: not-allowed;
}

/* RESPONSIVO */
@media (max-width: 900px) {
  .grid {
    grid-template-columns: repeat(2, 1fr);
  }
}

@media (max-width: 600px) {
  .grid {
    grid-template-columns: 1fr;
  }
}
</style>
