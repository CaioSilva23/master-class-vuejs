<template lang="">
    <div class='componente'>
        <h1>Componente Com Dados Reativos Não Primitivos</h1>
        <p>Nome: {{pessoa.nome}} | Idade: {{pessoa.idade}}</p>
        <button @click="fazerAniversario">Fazer Aniversário</button>
        <button @click="mudarNome">Mudar Nome</button>
    </div>
</template>
<!-- <script setup>
import { reactive } from 'vue';
const pessoa = reactive({
    nome: 'Fulano',
    idade: 30
});
const fazerAniversario = () => {
    pessoa.idade++;
}
const mudarNome = () => {
    pessoa.nome = 'João';
}
</script> -->

<script>
export default {
    data: () => {
        return {
            pessoa: {
                nome: 'Fulano',
                idade: 30
            }
        }
    },
    methods: {
        fazerAniversario() {
            this.pessoa.idade++;
        },
        mudarNome() {
            this.pessoa.nome = 'João';
        }
    }
}
</script>

<style>

</style>