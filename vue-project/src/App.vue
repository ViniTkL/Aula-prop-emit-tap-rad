<script setup>
import Formulario from './components/Formulario.vue';
import Tabela from './components/Tabela.vue';
import {ref, onMounted} from 'vue';
const pessoas = ref([
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
])

  const handleForm = (nome, cpf, categoria) => {
    alert(`${nome} ${cpf} ${categoria}`);
    const pessoaNova = {nome, cpf, categoria}

    pessoas.value[pessoas.value.length] = pessoaNova;
  }

  onMounted(async () => {
     await fetch('https://pokeapi.co/api/v2/pokemon')
    .then(result => result.json())
    .then(result2 => {
      pessoas.value = result2.results
    });
  })

</script>

<template>
  <main>
    <Formulario @salvar-pessoa="handleForm"/>
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
