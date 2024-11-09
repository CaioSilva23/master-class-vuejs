<template>
    <div class="componente">
        <h1>Componente com Data Binding</h1>
        <p>{{ valor }}</p>
        <input type="text" v-model="valor">
    </div>
</template>

<script setup>
import { ref } from 'vue';
const valor = ref('Data Binding');

</script>