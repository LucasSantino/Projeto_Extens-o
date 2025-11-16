<template>
  <section id="contato" class="contact">
    <div class="container">
      <h2>Contato</h2>
      <p><strong>Endereço:</strong> Parque Residencial São Clemente, Monte Mor - SP</p>
      <p><strong>Email:</strong> ong.arcoiris@gmail.com</p>
      <p><strong>Telefone:</strong> (19) 99999-9999</p>
    </div>
  </section>
</template>

<script lang="ts">
import { defineComponent } from "vue";
export default defineComponent({});
</script>

<style scoped>
.contact {
  padding: 80px 20px;
}
.container {
  max-width: 700px;
  margin: auto;
  text-align: center;
}
h2 {
  color: #ff4ec7;
  margin-bottom: 25px;
}
p {
  font-size: 18px;
  margin-bottom: 10px;
}
</style>
