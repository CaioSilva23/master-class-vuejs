<template lang="">
    <div class='componente'>
        <!-- <p :class="{'green': contador > 10}">Contador: {{ contador }}</p> -->
        <p :class="{'green': contador >= 10, 'red': contador < 10}">Contador: {{ contador }}</p>

        <button @click="incrementar">Incrementar</button>
        <button @click="decremetar">Decrementar</button>
        <div>
            <p v-if="contador % 2 === 0">Contador é par</p>
            <p v-else>Contador é ímpar</p>
        </div>
    </div>
</template>
<script>
export default {
    data: ()=>{
        return {
            contador: 0
        }
    },
    methods: {
        incrementar() {
            this.contador++;
        },
        decremetar() {
            this.contador--;
        }
    },

}
</script>
<style scoped>
.green {
    color: green;
}
.red {
    color: red;
}
</style>