<script setup>
    import {useRoute} from 'vue-router'
    import { ref } from 'vue'
    import productList from '@/assets/products.json'
    
    const nombre = ref("");
    const descripcion = ref("");

    const route= useRoute();
    for (const product of productList) {
        if (product.id==route.params.id) {
            nombre = product.name; 
            descripcion = product.description;   
        }
    
        console.log(`Nombre: ${nombre}, Descripción: ${descripcion}`);
    }
    
</script>

<template>
    <h1>Product Detail</h1>
    <h3>ID: {{ $route.params.id }}</h3>
    <p>Nombre: {{ nombre }}</p>
    <p>Descripción: {{ descripcion }}</p>

</template>

