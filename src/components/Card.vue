<template>
  <div class="card text-center">
    <h1>{{ figure }}</h1>

    <h3>{{ people }}</h3>
    <p>{{ subtext }}</p>

    <WhiteButton label="Learn More" />
  </div>
</template>

<style scoped>
.card {
  background: url("/src/assets/bluebadge.svg") top right/cover no-repeat;
  background-size: 180px;
  width: 400px;
  min-height: 350px;
  padding: 5rem 2rem 3rem;
  border: 1px solid #ccc;
  border-radius: 30px;
  display: flex;

  justify-content: center;
  flex-direction: column;
  margin: 0 0 3rem;
  text-align: center !important;
}

.card h1 {
  font-size: 3rem;
  opacity: 0.2;
  font-weight: bolder;
}

.card h3 {
  font-size: 2rem;
  margin: 2rem 0 0.8rem;
}

.card p {
  margin-bottom: 2.5rem;
  font-size: 1rem;
}

@media (max-width: 900px) {
  .card {
    width: 300px;
    min-height: 300px;
  }
}

@media (max-width: 600px) {
  .card {
    width: 100%;
  }
}
</style>
<script setup>
import WhiteButton from "./WhiteButton.vue";
import { defineProps } from "vue";

// Define props
const props = defineProps({
  figure: {
    type: Number,
    required: true,
  },
  people: {
    type: String,
  },
  subtext: {
    type: String,
  },
});
</script>
