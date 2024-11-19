<script setup>
import productList from '@/assets/products.json'
import{RouterLink} from 'vue-router'
</script>

<template>
    <ul>
        <li v-for="product in productList" :key="product.id">
            <RouterLink :to="'/detailProduct/' + product.id">{{ product.name }}</RouterLink>
        </li>
    </ul>
</template>

<style>

</style>