<style scoped>
.header-mail {
  gap: 0.4rem;
}
</style>

<template>
  <header class="header">
    <div class="container flex-between">
      <RouterLink class="flex-between header-mail" to="/">
        <img :src="mail" alt="" />
        <a href="mailto:hello@myshelta.com">hello@myshelta.com</a>
      </RouterLink>

      <div class="flex header-mail">
        <img :src="whatsapp" alt="" />
        <a href="https://wa.me/2348061796909?text="> +(234) 8061796909 </a>
      </div>
    </div>
  </header>
</template>

<script setup>
import mail from "@/assets/mail.svg";
import whatsapp from "@/assets/whatsapp.svg";
</script>
