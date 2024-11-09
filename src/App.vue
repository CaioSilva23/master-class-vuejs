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

const produto = "Camiseta";
const preco = 49.99;
const arrayCachorros = [
  {nome: 'Rex', idade: 10}, 
  {nome: 'Tobias', idade: 5}
]
</script>

<template>
  <header>Vue</header>
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
