<script setup>
const props = defineProps({
    title: {
      type: String,
      required: true,
    },
  });
</script>
<template>
<div class="card">
    <h1>{{ props.title }}</h1>
    <slot>
        conteudo
    </slot>
  </div>
</template>
<style scoped>
.card {
  border: 1px solid black;
  border-radius: 10px;
  width: 400px;
  padding: 20px;
  background-color: rgb(39, 39, 39);
  color: white;
}
</style>