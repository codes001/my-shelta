<script setup>
import HomeHero from "../components/HomeHero.vue";
import Header from "@/components/Header.vue";
import Navbar from "@/components/Navbar.vue";
</script>

<template>
  <main>
    <Header />
    <Navbar />
    <HomeHero />
  </main>
</template>

<style scoped>
main {
  min-height: 100vh;
  width: 100%;
}
</style>
