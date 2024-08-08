<script setup>
import { ref } from "vue";

const email = ref("");
const password = ref("");

const errors = ref({
  email: "",
  password: "",
});
</script>

<template>
  <header class="">
    <div class="container">
      <RouterLink to="/">
        <img
          width="120px"
          height="120px"
          src="/public/myshelta.jpeg"
          alt="MyShelta Logo"
        />
      </RouterLink>
    </div>
  </header>

  <form @submit.prevent="handleSubmit">
    <div class="flex-col">
      <h2>Login</h2>
      <p>Login to view your dashboard</p>
    </div>

    <div class="form-group">
      <label for="email"> Email Address </label>
      <input type="email" placeholder="Email Address" />
    </div>

    <div class="form-group">
      <label for="password"> Password </label>
      <input type="password" v-model="password" placeholder="Password" />
    </div>

    <button class="btn cursor-pointer" type="submit">Login</button>

    <div class="text-center">
      <p>
        Already have an account?
        <RouterLink to="/signup" class="blue-text cursor-pointer"
          >Sign Up</RouterLink
        >
      </p>
    </div>
  </form>
</template>

<script></script>

<style scoped>
header {
  height: max-content;
  margin-bottom: 4rem;
}
form {
  max-width: 500px;
  margin: 0 auto 2rem;
  padding: 1rem;
  /* border: 1px solid #ccc; */
}
.sign-up-tabs {
  gap: 0.5rem;
  margin: 1rem 0 2rem;
}
.sign-up-tabs span {
  background-color: #eee;
  padding: 0.7rem 1rem;
  width: 100%;
  border-radius: 0.4rem;
  text-align: center;
  cursor: pointer;
}

span.active {
  background-color: var(--bg-primary);
  color: var(--bg-white);
}

.form-group {
  display: flex;
  flex-direction: column;
}

label {
  margin: 1rem 0 0.6rem;
}

.sign-up-checkbox {
  margin: 1rem 0;
}
.sign-up-checkbox input {
  margin: 0 10px 0 0;
}

.btn {
  width: 100%;
  text-transform: uppercase;
  font-weight: semi-bold;
  padding: 1rem 0;
  margin: 1rem 0 1.4rem;
}

.blue-text {
  color: var(--bg-primary);
}
.lemon-green {
  color: #93b128;
}
</style>
