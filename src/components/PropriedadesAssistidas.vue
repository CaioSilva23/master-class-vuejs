<template>
    <div class="componente">
        <h1>Propriedades Assistidas</h1>
        <p>Idade: {{ idade }}</p>
        <label>Ano Nascimento:</label>
        <input type="number" v-model="anoNascimento" min="1900">
        <label>Ano Atual:</label>
        <input type="number" v-model="anoAtual" min="2000">
        <p></p>
    </div>
</template>

<script setup>
import { ref, watch, watchEffect } from 'vue';

const anoNascimento = ref(1990);
const anoAtual = ref(2000);
const idade = ref(0);

// watch(anoAtual, (anoAtual)=> {
//     idade.value = anoAtual - anoNascimento.value;
// })

// watch(anoNascimento, (anoNascimento)=> {
//     idade.value = anoAtual.value - anoNascimento;
// })

watchEffect(() => {
    idade.value = anoAtual.value - anoNascimento.value;
})
</script>

<style scoped>
label {
    margin: 10px;
}
</style>