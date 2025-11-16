<template>
  <header class="header">
    <div class="container">
      <h1 class="logo">ONG Arco-Íris</h1>
      <nav>
        <ul>
          <li><a href="#sobre">Sobre</a></li>
          <li><a href="#atividades">Atividades</a></li>
          <li><a href="#galeria">Fotos</a></li>
          <li><a href="#contato">Contato</a></li>
        </ul>
      </nav>
    </div>
  </header>
</template>

<script lang="ts">
import { defineComponent } from "vue";
export default defineComponent({});
</script>

<style scoped>
.header {
  background: #ffffff;
  padding: 20px 0;
  box-shadow: 0 2px 10px rgba(0,0,0,0.1);
  position: sticky;
  top: 0;
  z-index: 99;
}
.container {
  max-width: 1100px;
  margin: auto;
  display: flex;
  justify-content: space-between;
  align-items: center;
}
.logo {
  color: #ff7edb;
  font-weight: bold;
}
nav ul {
  display: flex;
  gap: 20px;
  list-style: none;
}
nav a {
  text-decoration: none;
  color: #444;
  font-weight: 600;
}
nav a:hover {
  color: #ff7edb;
}
</style>
