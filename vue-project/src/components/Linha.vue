<script setup>
    const props = defineProps(['pessoas'])
</script>

<template>
    <tr>
        <td>{{ pessoas.name}}</td>
        <td>{{ pessoas.nome}}</td>
        <td>{{ pessoas.cpf }}</td>
        <td>{{ pessoas.categoria }}</td>
        <td>{{ pessoas.acao }}</td>
    </tr>

</template>