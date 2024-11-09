<template lang="">
    <div class='componente'>
        <h1>Componente Com Dados Reativos Primitivos</h1>
        <p>Nome: {{nome}} | Idade: {{idade}}</p>
        <button @click="fazerAniversario">Fazer Aniversário</button>
        <button @click="mudarNome">Mudar Nome</button>
    </div>
</template>
<script setup>
import { ref } from 'vue';
    const nome = ref('Fulano');
    const idade = ref(30);

    const fazerAniversario = () => {
        idade.value++;
    }
    const mudarNome = () => {
        nome.value = 'João';
    }
</script>

<style>

</style>