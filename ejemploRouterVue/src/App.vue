<script setup>
import { RouterLink, RouterView } from 'vue-router'
</script>

<template>
      <nav>
        <RouterLink to="/">Home</RouterLink> <br>
        <RouterLink to="/about">About</RouterLink> <br>
        <RouterLink to="/contact">Contact</RouterLink> <br>
        <RouterLink to="/product">Products</RouterLink>
      </nav>
  <RouterView />
  
</template>

<style scoped>
</style>