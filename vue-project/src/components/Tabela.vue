<script setup>
    import Linha from './Linha.vue';
    const props = defineProps(['pessoas'])
</script>

<template>
    <table>
        <thead>
            <th>NOME</th>
            <th>CPF</th>
            <th>CATEGORIA</th>
            <th>AÇÕES</th>
        </thead>
    </table>
    <tbody>
        <Linha v-for="pessoa in pessoas" :pessoas="pessoa" />
    </tbody>
</template>