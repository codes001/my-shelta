<template>
  <button :class="type" :disabled="disabled">
    {{ label }}
  </button>
</template>

<style scoped>
button {
  padding: 10px 12px;
  font-size: 16px;
  border: none;
  border-radius: 5px;
  color: var(--primary);
  font-weight: 600;
  cursor: pointer;
  background: var(--secondary);
  /* font-size: 16px; */
}

button[disabled] {
  background-color: lightgrey;
  color: darkgrey;
  cursor: not-allowed;
}
</style>

<script setup>
import { defineProps } from "vue";

// Define props
const props = defineProps({
  label: {
    type: String,
    required: true,
  },
  type: {
    type: String,
    default: "button", // button, submit, reset
  },
  disabled: {
    type: Boolean,
    default: false,
  },
});
</script>
