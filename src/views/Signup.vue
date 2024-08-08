<script setup>
import { ref } from "vue";
const firstName = ref("");
const lastName = ref("");
const email = ref("");
const password = ref("");
const confirmPassword = ref("");
const inviteCode = ref("");
const partnerCheck = ref("");
const errors = ref({
  firstName: "",
  lastName: "",
  email: "",
  password: "",
  confirmPassword: "",
  inviteCode: "",
  partnerCheck: "",
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
      <h2>Register</h2>
      <p>Sign up for free and gain exclusive access</p>
    </div>

    <div class="flex sign-up-tabs">
      <span class="active">Individual</span>
      <span>Organization</span>
    </div>

    <div class="form-group">
      <label for="firstName"> First Name </label>
      <input type="text" v-model="firstName" placeholder="First Name" />
    </div>
    <div class="form-group">
      <label for="lastName"> Last Name </label>
      <input type="text" v-model="lastName" placeholder="Last Name" />
    </div>
    <div class="form-group">
      <label for="email"> Email Address </label>
      <input type="email" placeholder="Email Address" />
    </div>
    <div class="form-group">
      <label for="password"> Password </label>
      <input type="password" v-model="password" placeholder="Password" />
    </div>
    <div class="form-group">
      <label for="confirmPassword"> Confirm Password </label>
      <input
        type="password"
        v-model="confirmPassword"
        placeholder="Confirm Password"
      />
    </div>
    <div class="form-group">
      <label for="inviteCode"> Invite Code </label>
      <input type="text" v-model="inviteCode" placeholder="Enter invite code" />
    </div>

    <div class="sign-up-checkbox">
      <input
        type="checkbox"
        v-model="partnerCheck"
        id="partnerCheck"
        value="partnerCheck"
      />
      <span>Are you a partner?</span>
    </div>

    <button class="btn" type="submit">Create my account</button>

    <div class="text-center flex-col" style="gap: 1rem">
      <p class="blue-text">
        By clicking the "Create My Account" button, you agree to Shelta's
        <a href="#" class="lemon-green"> terms and conditions </a>
      </p>

      <p>
        Already have an account?
        <RouterLink to="/login" class="blue-text">Login</RouterLink>
      </p>
    </div>
  </form>

  <footer></footer>
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

footer {
  background-color: #034aed;
  width: 100%;
  margin-top: 2rem;
  height: 80px;
  overflow: hidden;
  text-align: center;
  color: #fff;
}
</style>
