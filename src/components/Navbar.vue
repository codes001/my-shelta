
<style scoped>

nav{
  box-shadow: 1px 3px 10px rgba(239, 231, 224, 0.7);
  padding: .5rem 0;
  height: 70px;
}
nav .container{
  justify-content: space-between;
  align-items: center;
  
}

.navbar-ul{
  gap: 1rem;
  align-items: center;
}

@media(max-width:768px){
  .nav .navbar-ul{
    display: none;
  }
}
</style>

<template>
  <nav class="nav ">
    <div class="container flex">
      <RouterLink to="/">
        <img src="/myshelta.jpeg" class="logo" alt="myShelta" />
      </RouterLink>
    

      <ul class="flex navbar-ul">
        <li v-for="link in navbarLinks" :key="link.text">
          <RouterLink :to="link.url">{{ link.text }}</RouterLink>
        </li>
      
        <WhiteButton
        label="Sign Up"
        type="button"
      />  

      <Button
        label="Sign Up"
        type="button"
      />    
      </ul>

      <!-- <div class="menu">
        <img src="src/assets/hamburger.svg" alt="">
      </div> -->
    </div>
  </nav>
</template>

<script setup>
import { navbarLinks } from "@/utils";
import Button from '@/components/Button.vue'
import WhiteButton from '@/components/WhiteButton.vue'
// import hamburger from '@/assets/hamburger.svg'

</script>
