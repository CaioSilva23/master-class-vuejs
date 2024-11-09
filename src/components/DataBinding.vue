<template>
    <div class="componente">
        <h1>Componente com Data Binding</h1>
        <p>{{ valor }}</p>
        <!-- <input 
            v-bind:value="valor"
            v-on:input="(e)=> valor = e.target.value"
            type="=text"
        > -->
        <!-- <input 
            :value="valor" 
            @:input="(e)=> valor = e.target.value" 
            type="text"
        > -->
        <input type="text" v-model="valor">
    </div>
</template>

<script setup>
import { ref } from 'vue';
const valor = ref('Data Binding');

</script>