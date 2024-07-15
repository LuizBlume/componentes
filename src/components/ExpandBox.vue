<script setup>
import { ref, computed } from 'vue'
const ShowBox = ref(false)
const textButton = computed(() => ShowBox.value ? 'Esconder' : 'Mostrar')
// const props = defineProps (['title', 'content'])
defineProps({
    title: {
    type: String,
    required: true,
},
content: {
    type: String,
    default: 'Valor padrão da minha caixa'
}
})
</script>

<template>
<div class="ShowBoxArea">
    <button @click="ShowBox = !ShowBox" >{{textButton }}</button>
    <div v-if="ShowBox" class="expand-box">
        <h1>{{ title }}</h1>
        <p>{{ content }}</p>
        <img src="" alt="">
    </div>
</div>
</template>

<style scoped>
.ShowBoxArea{
    border: 1px solid black;
    border-radius: 10px;
    width: 400px;
    padding: 20px;
    background-color: rgb(39, 39, 39);
}



.expand-box p{
    background-color: black;
    color: greenyellow;
    font-family: monospace;
    padding: 10px;
}

button{
    text-align: center;
    background-color: black;
    color: white;
    border: 1px solid gray;
    padding: 10px;
}
h1{
    font-size: 1em;
    color: white;
    text-align: center;
    font-family: monospace;
}

</style>