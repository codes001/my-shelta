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
        <p>hello@myshelta.com</p>
      </RouterLink>

      <div class="flex header-mail">
        <img :src="whatsapp" alt="" />
        <a href="#"> +(234) 8061796909 </a>
      </div>
    </div>
  </header>
</template>

<script setup>
import mail from '@/assets/mail.svg';
import whatsapp from '@/assets/whatsapp.svg';
</script>
