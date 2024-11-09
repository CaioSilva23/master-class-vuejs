<template lang="">
    <div class="componente">
        <h1>Componente com props</h1>
        <p>{{ item }} R${{preco}}</p>
        
    </div>
</template>
<script setup>
import { defineProps } from 'vue';
defineProps({
    item: String,
    preco: Number
});
</script>
<!-- <script>
export default {
    data() {
        return {
            item: 'Camiseta',
            preco: 49.99
        }
    }
} -->
<!-- </script> -->
<style lang="">
    
</style>