<script setup>
    import {ref} from 'vue';
    const emit = defineEmits(['salvar-pessoa'])

    const nome = ref('');
    const cpf = ref('');
    const categoria = ref('');

    const onSubmit = () => {
        emit('salvar-pessoa', nome.value, cpf.value, categoria.value)
    }
</script>
<template>
    <form @submit.prevent="onSubmit">
        <div>
            <label for="nome">Nome</label>
            <input type="text" id="nome" v-model="nome">
        </div>
        <div>
            <label for="CPF">CPF</label>
            <input type="text" id="CPF" v-model="cpf">
        </div>
        <div>
            <label for="CATEGORIA">CATEGORIA</label>
            <input type="text" id="CATEGORIA" v-model="categoria">
        </div>
      

        <button>Salvar</button>
    </form>
</template>