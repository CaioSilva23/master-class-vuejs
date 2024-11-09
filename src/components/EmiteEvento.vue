<template lang="">
    <div class="componente">
        <h1>Emite Evento</h1>
        <p>{{ item }} R${{preco}}</p>
        <button @click="adicionar">Adicionar ao carrinho</button>
    </div>
</template>
<script>
export default {
  props: {
    item: {
      type: String,
      required: true
    },
    preco: {
      type: Number,
      required: true
    }
  },
  emits: ['adicionar'],
  methods: {
    adicionar() {
      this.$emit('adicionar', this.preco);
    }
  }
}
</script>
<!-- <script setup>
import { defineProps, defineEmits } from 'vue';

const {item, preco} = defineProps({
    item: String,
    preco: Number
});

const emit = defineEmits(['adicionar']);

const adicionar = () => {
    emit('adicionar', preco);
}
</script> -->
<style lang="">
    
</style>