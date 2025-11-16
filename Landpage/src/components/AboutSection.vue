<template>
  <section id="sobre" class="about-section">
    <div class="container">
      <h2>Sobre a ONG Arco-Íris</h2>
      <p>
        A ONG Arco-Íris atua no apoio às famílias do bairro São Clemente,
        desenvolvendo iniciativas sociais que promovem bem-estar, educação,
        solidariedade e inclusão. O objetivo é transformar a realidade da
        comunidade através de projetos voluntários e atividades culturais.
      </p>
    </div>
  </section>
</template>

<script lang="ts">
import { defineComponent } from "vue";
export default defineComponent({});
</script>

<style scoped>
.about-section {
  padding: 80px 20px;
  background: #fff7fd;
}
.container {
  max-width: 900px;
  margin: auto;
}
h2 {
  text-align: center;
  margin-bottom: 25px;
  color: #ff4ec7;
}
p {
  font-size: 18px;
  line-height: 1.6;
  text-align: center;
}
</style>
