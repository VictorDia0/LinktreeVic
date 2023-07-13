<script setup>
import Item from "./components/item.vue";
</script>

<script>
import Dados from "./Dados/services.json";
export default {
  data() {
    return {
      servicos: null,
    };
  },
  mounted() {
    this.servicos = Dados;
  },
};
</script>

<template>
  <div class="logo">
    <img alt="Vue logo" src="src/Dados/img/minhafoto.png" /><span
      id="nome"
      >Victor Dias Pereira</span
    >
  </div>
  <div class="items">
    <Item v-for="(servico, index) in servicos" :key="index" :item="servico" />
  </div>
</template>

<style scoped>
.logo {
  display: flex;
  justify-content: center;
  align-items: center;
  flex-direction: column;
}

.logo img {
  width: 200px;
  height: 200px;
}
.items {
  display: flex;
  align-items: center;
  justify-content: center;
  margin: 0 auto;
}

#nome {
  display: flex;
  justify-content: center;
  align-items: center;
  margin-top: 10px;
  font-size: x-large;
  color: white;
}

@media (max-width: 768px) {
  .items {
    flex-wrap: wrap;
  }
}

@media (max-width: 768px) {
  .logo {
    display: flex;
    justify-content: center;
    align-items: center;
  }
}
</style>
