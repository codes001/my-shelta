<script setup>
import { RouterLink, RouterView } from "vue-router";
import HelloWorld from "./components/HelloWorld.vue";
import Navbar from "./components/Navbar.vue";
import Header from "./components/Header.vue";
import { navbarLinks } from "./utils";
import HomeView from "./views/HomeView.vue";
</script>

<template>
  <RouterView />
</template>

<style></style>
