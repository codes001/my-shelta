<template>
  <Header />
  <Navbar />
</template>

<style>
@media (min-width: 1024px) {
  .about {
    min-height: 100vh;
    display: flex;
    align-items: center;
  }
}
</style>

<script setup>
import Header from "@/components/Header.vue";
import Navbar from "@/components/Navbar.vue";
</script>
