<template>
  <section id="atividades" class="activities">
    <div class="container">
      <h2>Atividades</h2>

      <div class="cards">
        <div class="card" v-for="item in activities" :key="item.title">
          <img :src="item.image" alt="atividade" />
          <h3>{{ item.title }}</h3>
          <p>{{ item.description }}</p>
        </div>
      </div>

    </div>
  </section>
</template>

<script lang="ts">
import { defineComponent } from "vue";

export default defineComponent({
  data() {
    return {
      activities: [
        {
          title: "Apoio a Famílias",
          description: "Doações de alimentos, roupas e itens essenciais.",
          image: "https://images.unsplash.com/photo-1607746882042-944635dfe10e",
        },
        {
          title: "Atividades Educacionais",
          description: "Reflexão, reforço escolar e desenvolvimento infantil.",
          image: "https://images.unsplash.com/photo-1588072432836-e10032774350",
        },
        {
          title: "Ações Comunitárias",
          description: "Eventos, mutirões e campanhas solidárias.",
          image: "https://images.unsplash.com/photo-1521737604893-d14cc237f11d",
        }
      ]
    };
  }
});
</script>

<style scoped>
.activities {
  padding: 80px 20px;
}
h2 {
  text-align: center;
  margin-bottom: 40px;
  color: #ff4ec7;
}
.cards {
  display: flex;
  gap: 25px;
  justify-content: center;
  flex-wrap: wrap;
}
.card {
  width: 300px;
  background: white;
  border-radius: 10px;
  box-shadow: 0 4px 12px rgba(0,0,0,0.1);
  padding-bottom: 20px;
  text-align: center;
}
.card img {
  width: 100%;
  border-radius: 10px 10px 0 0;
}
.card h3 {
  margin: 20px 0 10px;
  color: #ff4ec7;
}
.card p {
  padding: 0 15px;
  font-size: 15px;
}
</style>
