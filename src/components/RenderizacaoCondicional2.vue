<template lang="">
    <div class='componente'>
        <h1>Componente com RenderizacaoCondicional</h1>
        <p>Nome: {{ nome }}</p>
        <p v-if="qtdCachorro === 0"> Não tem cachorro</p>
        <p v-else-if="qtdCachorro === 1"> Tem {{qtdCachorro}} cachorro</p>
        <p v-else> Tem {{qtdCachorro}} cachorros</p>
    </div>
</template>
<script setup>
import { defineProps } from 'vue';
defineProps({
    nome: String,
    qtdCachorro: Number
})
</script>
<style scoped>

</style>