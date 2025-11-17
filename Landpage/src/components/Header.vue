<template>
  <header class="navbar">
    <div class="navbar-content">
      <img
        src="@/assets/images/Logosemfundo.png"
        alt="Logo ONG Arco-Íris"
        class="logo"
      />

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
</script>

<style scoped>
.navbar {
  width: 100%;
  background-color: #1d3557;
  padding: 12px 40px;
  display: flex;
  justify-content: center;
  box-shadow: 0px 2px 6px rgba(0,0,0,0.15);
  position: fixed;
  top: 0;
  left: 0;
  z-index: 10;
}

.navbar-content {
  width: 100%;
  max-width: 1400px;
  display: flex;
  align-items: center;
  justify-content: space-between;
}

.logo {
  height: 55px;
  object-fit: contain;
  border-radius: 4px;
}

.nav-links {
  display: flex;
  gap: 28px;
}

.nav-links a {
  color: #ffffff;
  text-decoration: none;
  font-size: 1.05rem;
  font-weight: 500;
  transition: 0.3s;
}

.nav-links a:hover {
  opacity: 0.7;
}
</style>
