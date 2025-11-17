<template>
  <section class="hero">
    <img
      src="@/assets/images/banner-ongArcoiris.jpg"
      alt="Banner ONG Arco-Íris"
      class="hero-img"
    />

    <div class="hero-overlay">
      <h1 class="hero-title">
        União e Solidariedade: Construindo o Amanhã, Transformando o Agora.
      </h1>

      <button class="hero-btn" @click="scrollToAbout">
        Saiba mais sobre nós!!
      </button>
    </div>
  </section>
</template>

<script setup lang="ts">
const scrollToAbout = () => {
  const el = document.getElementById("about");
  if (el) el.scrollIntoView({ behavior: "smooth" });
};
</script>

<style scoped>
:host {
  display: block;
  padding: 0;
  margin: 0;
}

/* ---- HERO ---- */
.hero {
  position: relative;
  width: 100vw;
  height: 92vh;
  overflow: hidden;

  left: 50%;
  right: 50%;
  margin-left: -50vw;
  margin-right: -50vw;
}

.hero-img {
  width: 100%;
  height: 100%;
  object-fit: cover;
  display: block;
}

/* ---- OVERLAY ---- */
.hero-overlay {
  position: absolute;
  inset: 0;

  display: flex;
  flex-direction: column;
  justify-content: center;

  /* alinhamento à esquerda */
  align-items: flex-start;

  text-align: left;

  background: rgba(0, 0, 0, 0.60);
  padding: 40px 60px;
}

/* ---- TEXTO ---- */
.hero-title {
  color: #ffffff;
  font-size: 2.9rem;
  font-weight: 700;
  max-width: 900px;
  margin-bottom: 32px;
}

/* ---- BOTÃO ---- */
.hero-btn {
  background: #1d3557;
  color: #ffffff;
  border: none;

  padding: 15px 45px;
  font-size: 1.2rem;

  border-radius: 12px;
  cursor: pointer;

  transition: transform 0.3s ease, background 0.3s ease, box-shadow 0.3s ease;
}

/* efeito hover com “movimento” */
.hero-btn:hover {
  background: #3d6da8;
  transform: translateY(-3px) scale(1.03);
  box-shadow: 0px 6px 18px rgba(0, 0, 0, 0.35);
}

/* ---- RESPONSIVO ---- */
@media (max-width: 780px) {
  .hero-overlay {
    padding: 20px;
    align-items: flex-start;
  }

  .hero-title {
    font-size: 2.1rem;
    max-width: 95%;
  }

  .hero-btn {
    font-size: 1.1rem;
    padding: 12px 30px;
    border-radius: 10px;
  }
}
</style>
