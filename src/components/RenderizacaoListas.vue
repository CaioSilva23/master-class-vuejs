<template lang="">
    <div class='componente'>
        <h1>Componente com Renderizacao de Listas</h1>
        <p>Nome: {{ nome }}</p>
        <ul v-if="arrayCachorros.length > 1">
            <li v-for="cachorro in arrayCachorros" :key="cachorro">
                Nome: {{ cachorro.nome }} | Idade: {{ cachorro.idade }}
            </li>
        </ul>
        <!-- <p v-else> Não tem cachorros </p> -->
        <p v-show="arrayCachorros.length === 0">Não tem cachorros</p>
    </div>
</template>

<script>
export default {
    props: {
        nome: String,
        arrayCachorros: Array
    }
}
</script>

<!-- <script setup>
import { defineProps } from 'vue';
defineProps({
    nome: String,
    arrayCachorros: Array
})
</script> -->


<style scoped>
ul {
  margin: 0px;
  padding: 0px;

}
li {
  list-style: none;
  text-align: center;
  font-size: large;
}
</style>