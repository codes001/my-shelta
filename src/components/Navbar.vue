<style scoped>
nav {
  box-shadow: 1px 3px 10px rgba(239, 231, 224, 0.7);
  padding: 0.5rem 0;
  height: 70px;
}
nav .container {
  justify-content: space-between;
  align-items: center;
}

.navbar-ul {
  gap: 1rem;
  align-items: center;
}

.menu {
  display: none;
}
/*  */

/* Mobile Menu Styling */
.mobile-menu {
  transition: all 1s ease-in-out;
  display: none;
  flex-direction: column;
  position: absolute;
  top: 80px;
  right: 0;
  background-color: var(--secondary);
  width: 100%;
  text-align: center;
  list-style: none;
  padding: 0;
  margin: 0;
}

.mobile-menu.nav-active {
  display: flex;
}

.mobile-menu li {
  padding: 1rem 0;
}

@media (max-width: 768px) {
  .nav .navbar-ul {
    display: none;
  }

  .menu {
    display: block;
  }
}

@media (min-width: 769px) {
  .mobile-menu {
    display: none;
  }
}
</style>

<template>
  <nav class="nav">
    <div class="container flex">
      <RouterLink to="/">
        <img src="/myshelta.jpeg" class="logo" alt="myShelta" />
      </RouterLink>

      <ul class="flex navbar-ul">
        <li v-for="link in navbarLinks" :key="link.text">
          <RouterLink :to="link.url">{{ link.text }}</RouterLink>
        </li>

        <WhiteButton label="Sign Up" type="button" />

        <Button label="Sign Up" type="button" />
      </ul>

      <div class="menu cursor-pointer">
        <svg
          class="menu-icon"
          @click="toggleMenu"
          width="20"
          height="18"
          viewBox="0 0 29 18"
          fill="none"
          xmlns="http://www.w3.org/2000/svg"
        >
          <path
            d="M1 8.99911H28"
            stroke="#FFB100"
            stroke-width="2"
            stroke-linecap="round"
            stroke-linejoin="round"
          />
          <path
            d="M1 0.999107H28"
            stroke="#FFB100"
            stroke-width="2"
            stroke-linecap="round"
            stroke-linejoin="round"
          />
          <path
            d="M1 16.9991H23"
            stroke="#FFB100"
            stroke-width="2"
            stroke-linecap="round"
            stroke-linejoin="round"
          />
          <path
            d="M27 16.9991H28"
            stroke="#FFB100"
            stroke-width="2"
            stroke-linecap="round"
            stroke-linejoin="round"
          />
        </svg>
      </div>

      <!-- Mobile Menu -->
      <ul :class="{ 'mobile-menu': true, 'nav-active': isMenuOpen }">
        <li v-for="link in navbarLinks" :key="link.text">
          <RouterLink :to="link.url">{{ link.text }}</RouterLink>
        </li>
      </ul>
    </div>
  </nav>
</template>

<script setup>
import { navbarLinks } from "@/utils";
import Button from "@/components/Button.vue";
import WhiteButton from "@/components/WhiteButton.vue";
import { ref } from "vue";

const isMenuOpen = ref(false);

function toggleMenu() {
  isMenuOpen.value = !isMenuOpen.value;
}

//INITIALIZE
</script>
