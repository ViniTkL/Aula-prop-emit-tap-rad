<script setup>
import Tabela from './components/Tabela.vue';

const pessoas = [
  {
    nome: 'Pessa',
    cpf: '111.111.111-11',
    categoria: 'A'
  },
  {
    nome: 'Pesasdasdasdsa',
    cpf: '222.111.222-11',
    categoria: 'B'
  },
  {
    nome: 'sadasdasdasdasf sgsw ewg',
    cpf: '025.658.111-45',
    categoria: 'C'
  }
]
</script>

<template>
  <main>
    <Tabela  :pessoas="pessoas"/>
  </main>
</template>

<style scoped>
header {
  line-height: 1.5;
}

.logo {
  display: block;
  margin: 0 auto 2rem;
}

@media (min-width: 1024px) {
  header {
    display: flex;
    place-items: center;
    padding-right: calc(var(--section-gap) / 2);
  }

  .logo {
    margin: 0 2rem 0 0;
  }

  header .wrapper {
    display: flex;
    place-items: flex-start;
    flex-wrap: wrap;
  }
}
</style>
