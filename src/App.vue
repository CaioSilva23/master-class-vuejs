<script setup>
import PrimeiroComponente from './components/PrimeiroComponente.vue';
import ComDados from './components/ComDados.vue';
import ComDadosReativosPrimitivos from './components/DadosReativosPrimitivos.vue';
import ComDadosReativosNaoPrimitivos from './components/DadosReativosNaoPrimitivos.vue';
import DataBinding from './components/DataBinding.vue';
import ComProps from './components/ComProps.vue';
import EscutaEvento from './components/EscutaEvento.vue';
import PropriedadesComputadas from './components/PropriedadesComputadas.vue';
import PropriedadesAssistidas from './components/PropriedadesAssistidas.vue';
import RenderizacaoCondicional from './components/RenderizacaoCondicional.vue';
import RenderizacaoCondicional2 from './components/RenderizacaoCondicional2.vue';
import RenderizacaoListas from './components/RenderizacaoListas.vue';
import Slots from './components/Slots.vue';

const produto = "Camiseta";
const preco = 49.99;
const arrayCachorros = [
  {nome: 'Rex', idade: 10}, 
  {nome: 'Tobias', idade: 5}
]
</script>

<template>
  <header>Vue</header>
  <Slots>
    <template v-slot:icone>
      <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-linecap="round" stroke-linejoin="round" width="24" height="24" stroke-width="2"> 
        <path d="M5 12l-2 0l9 -9l9 9l-2 0"></path>
        <path d="M5 12v7a2 2 0 0 0 2 2h10a2 2 0 0 0 2 -2v-7"></path>
        <path d="M10 12h4v4h-4z"></path> 
      </svg>
    </template>
    <template v-slot:texto>
      Home
    </template>
  </Slots>
  <RenderizacaoListas nome="Francisca" :arrayCachorros="arrayCachorros"/>
  <RenderizacaoCondicional2 nome="Francisca" :qtdCachorro="10"/>
  <RenderizacaoCondicional/>
  <PropriedadesAssistidas/>
  <PropriedadesComputadas/>
  <EscutaEvento/>
  <ComProps :item="produto" :preco="preco"/>
  <DataBinding/>
  <ComDadosReativosNaoPrimitivos/>
  <ComDadosReativosPrimitivos/>
  <ComDados/>
  <PrimeiroComponente/>
</template>

<style scoped>

</style>
