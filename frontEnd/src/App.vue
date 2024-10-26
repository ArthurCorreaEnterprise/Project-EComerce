<template>
  <header>
    <NavBar />
  </header>

  <RouterView />
</template>

<script setup>
import { RouterView } from 'vue-router'
import NavBar from './components/Navbar.vue'
</script>

<style scoped></style>
