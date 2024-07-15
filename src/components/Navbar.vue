<style scoped></style>

<template>
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

<script setup></script>
