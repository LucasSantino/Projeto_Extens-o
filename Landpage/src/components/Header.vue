<template>
  <header :class="['navbar', { transparent: isScrolled }]">
    <div class="navbar-content">

      <div class="logo-area">
        <img
          src="@/assets/images/Logosemfundo.png"
          alt="Logo ONG Arco-Íris"
          class="logo"
        />
        <span class="ong-name">ONG Arco-Íris</span>
      </div>

      <nav class="nav-links">
        <a href="#about">Sobre</a>
        <a href="#activities">Atividades</a>
        <a href="#gallery">Galeria</a>
        <a href="#contact">Contato</a>
      </nav>
      
    </div>
  </header>
</template>

<script setup lang="ts">
import { ref, onMounted, onUnmounted } from "vue";

const isScrolled = ref(false);

const handleScroll = () => {
  isScrolled.value = window.scrollY > 20;
};

onMounted(() => window.addEventListener("scroll", handleScroll));
onUnmounted(() => window.removeEventListener("scroll", handleScroll));
</script>

<style scoped>
.navbar {
  width: 100%;
  background-color: #1d3557;
  padding: 14px 50px;
  display: flex;
  justify-content: center;
  box-shadow: 0px 2px 6px rgba(0, 0, 0, 0.15);
  position: fixed;
  top: 0;
  left: 0;
  z-index: 10;
  transition: background-color 0.35s ease-in-out, backdrop-filter 0.35s;
}

.navbar.transparent {
  background-color: rgba(29, 53, 87, 0.25);
  backdrop-filter: blur(6px);
}

.navbar-content {
  width: 100%;
  max-width: 1400px;
  display: flex;
  align-items: center;
  justify-content: space-between;
}

.logo-area {
  display: flex;
  align-items: center;
  gap: 14px;
}

.logo {
  height: 75px; /* AUMENTADO */
  object-fit: contain;
}

.ong-name {
  font-size: 1.4rem;
  font-weight: 600;
  color: white;
  letter-spacing: 1px;
}

.nav-links {
  display: flex;
  gap: 56px; /* MAIS ESPAÇO ENTRE OPÇÕES */
}

.nav-links a {
  color: #ffffff;
  text-decoration: none;
  font-size: 1.12rem;
  font-weight: 500;
  position: relative;
  padding-bottom: 3px;
  transition: color 0.3s ease-in-out;
}

/* underline suave apenas no hover */
.nav-links a::after {
  content: "";
  width: 0%;
  height: 2px;
  background-color: #ffffff;
  position: absolute;
  left: 0;
  bottom: 0;
  transition: width 0.25s ease-in-out;
}

.nav-links a:hover::after {
  width: 100%;
}
</style>
