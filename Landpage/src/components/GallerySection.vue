<template>
  <section id="galeria" class="gallery">
    <h2>Galeria de Fotos</h2>

    <div class="grid">
      <img v-for="n in 6" :key="n"
        :src="`https://source.unsplash.com/random/300x300?community&sig=${n}`"
        alt="foto da ong"
      />
    </div>
  </section>
</template>

<script lang="ts">
import { defineComponent } from "vue";
export default defineComponent({});
</script>

<style scoped>
.gallery {
  padding: 80px 20px;
  background: #fff7fd;
}
h2 {
  text-align: center;
  margin-bottom: 40px;
  color: #ff4ec7;
}
.grid {
  max-width: 1000px;
  margin: auto;
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
  gap: 15px;
}
.grid img {
  width: 100%;
  border-radius: 8px;
}
</style>
