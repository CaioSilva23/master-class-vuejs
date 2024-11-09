<template>
    <div class='componente'>
        <h1>Componente com dados</h1>
        <p>Nome: {{nome}} - {{ codigo }}</p>
    </div>
</template>

<!-- <script>
// options API
export default {
    data: ()=>{
        return {
            nome: 'Caneta1',
            codigo: '#12ewew3'
        }
    }
}

// Composition API
export default {
    setup() {
        const nome = "Lapis";
        const codigo = "#123456";
        return { nome, codigo }
    }
}
</script> -->

<script setup>

const nome = "Apontador";
const codigo = "#123456";

</script>

<style scoped>
</style>