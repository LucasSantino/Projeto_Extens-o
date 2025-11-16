<template>
  <footer class="footer">
    <p>© {{ year }} ONG Arco-Íris — Todos os direitos reservados.</p>
  </footer>
</template>

<script lang="ts">
import { defineComponent } from "vue";

export default defineComponent({
  data() {
    return {
      year: new Date().getFullYear()
    };
  }
});
</script>

<style scoped>
.footer {
  background: #ff7edb;
  color: white;
  padding: 20px;
  text-align: center;
  margin-top: 40px;
}
</style>
