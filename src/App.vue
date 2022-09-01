<script setup>
import { ref } from "vue";
import ArticuloDetalle from "./components/ArticuloDetalle.vue";

const articulos = ref([]);


//fetch('https://jsonplaceholder.typicode.com/posts/',{
fetch("http://localhost:3001/articulos"
//,{mode:"cors"}
)
    .then(res => res.json())
    .then(data => articulos.value = data)
    .then(console.log(articulos.value))
    .catch(e=>console.log(e))

</script>

<template>
    <div class="container">

        <h1>API a Vue</h1>
        <ArticuloDetalle 
        v-for="articulo in articulos" 
        :key="articulo.id" 
        :title="articulo.codigo"
        :body="articulo.descripcion"
        />
    </div>
</template>
