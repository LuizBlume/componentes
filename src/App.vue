<script setup>
import ExpandBox from './components/ExpandBox.vue';
import CardComp from './components/CardComp.vue';
import CardFull from './components/CardFull.vue';
const caixas = [
  { id: 1, title: 'Caixa', content: 'Quantidade 1' },
  { id: 2, title: 'Caixa', qty: '100' },
  { id: 3, title: 'Caixa', content: 'Quantidade 1', qty: '100' },
  { id: 4, title: 'Caixa', content: 'Quantidade 1', qty: '100' },
]
</script>

<template>
  <h1>Componentes</h1>
  <hr>
  <expand-box v-for="caixa in caixas" :key="caixa.id" v-bind="caixa" />
  <CardComp title="Título do card">
    <p>Conteúdo do card</p>
  </CardComp>
  <CardComp title="Título do card 2">
    <p>Conteúdo do card 2</p>
  </CardComp>
  <CardFull>
    <p>Body</p>
    <template #header>
      <h1>Header</h1>
    </template>
    <template #footer>
      <p>Footer</p>
    </template>
  </CardFull>
  <!-- <ExpandBox title="caixa 1" content="Lorem, ipsum dolor sit amet consectetur adipisicing elit. Architecto soluta necessitatibus, cupiditate voluptates amet nulla magnam natus optio totam tempore quaerat iure suscipit aspernatur tempora, labore veritatis fuga, fugit nesciunt"/>
  <ExpandBox title="caixa 2"/> -->
</template>

<style scoped></style>
