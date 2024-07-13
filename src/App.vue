<script setup>
import { RouterLink, RouterView } from 'vue-router';
import HelloWorld from './components/HelloWorld.vue';

import { navbarLinks } from './utils/index.vue';
</script>

<template>
  <header class="header">
    <div class="container flex-between">
      <RouterLink to="/">
        <p>hello@myshelta.com</p>
      </RouterLink>

      <a href="#"> +(234) 8061796909 </a>
    </div>
  </header>

  <nav class="nav">
    <div class="container">
      <RouterLink to="/">
        <img src="/myshelta.jpeg" class="logo" alt="myShelta" />
      </RouterLink>
      <!-- <RouterLink to="/">Home</RouterLink>
    <RouterLink to="/about">About</RouterLink> -->

      <ul>
        <li class="flex" v-for="link in links" :key="link.text">
          <RouterLink :to="link.url">{{ link.text }}</RouterLink>
        </li>
      </ul>
    </div>
  </nav>
</template>

<style scoped>
header {
  background-color: var(--primary);
  width: 100%;
  height: 35px;
  color: #fff;
  padding: 5px 0;
}
header .container {
  align-items: center;
}
.logo {
  width: 50px;
  aspect-ratio: 1/1;
}

.nav {
  background: #ccc;
  height: 50px;
}
</style>
