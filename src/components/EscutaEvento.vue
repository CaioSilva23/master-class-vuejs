<template lang="">
    <div class="componente">
        <h1>Componente que Escuta Evento</h1>
        <p>Total: R$ {{total}}</p>
        <div class="lista">
            <EmiteEvento 
                item="Item1" 
                :preco="19.90" 
                @adicionar="atualizarTotal"
            />
            <EmiteEvento 
                item="Item2" 
                :preco="10.99"
                @adicionar="atualizarTotal"
            />
            <EmiteEvento 
                item="Item3" 
                :preco="5.90"
                @adicionar="atualizarTotal"
            />
        </div>
    </div>
</template>

<script setup>
import { ref } from 'vue';
import EmiteEvento from './EmiteEvento.vue';

const total = ref(0);

const atualizarTotal = (p) => {
    const valor = total.value + p;
    total.value = +valor.toFixed(2);
}

</script>

<style>
.lista{
    display: flex;
    justify-content: space-between;
}
</style>