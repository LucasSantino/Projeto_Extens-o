<template>
  <section class="hero">
    <div class="overlay">
      <h2>Transformando vidas com solidariedade</h2>
      <p>A ONG Arco-Íris atua pela inclusão e apoio à comunidade.</p>
      <a href="#sobre" class="btn">Saiba Mais</a>
    </div>
  </section>
</template>

<script lang="ts">
import { defineComponent } from "vue";
export default defineComponent({});
</script>

<style scoped>
.hero {
  height: 75vh;
  background: url("https://images.unsplash.com/photo-1526256262350-7da7584cf5eb") center/cover no-repeat;
  position: relative;
}
.overlay {
  background: rgba(0,0,0,0.4);
  height: 100%;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  color: white;
  text-align: center;
  padding: 0 20px;
}
.btn {
  margin-top: 20px;
  background: #ff7edb;
  color: white;
  padding: 12px 25px;
  text-decoration: none;
  font-weight: bold;
  border-radius: 6px;
}
.btn:hover {
  background: #ff4ec7;
}
</style>
