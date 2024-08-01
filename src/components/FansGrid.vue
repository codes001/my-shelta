<template>
  <section class="w-full">
    <div class="container fans-grid">
      <div class="grid-item grid-item-1">
        <h2>Loved by 10,000+ Africans</h2>

        <hr style="width: 100px; text-align: center" />

        <Button label="Create a free account" type="button" />
      </div>

      <div class="fans-grid-main">
        <img class="grid-item" :src="a" alt="a" />
        <img :src="b" alt="b" />
        <img :src="c" alt="c" />
        <img :src="d" alt="d" />
        <img :src="e" alt="e" />
        <img :src="f" alt="f" />
        <img :src="g" alt="g" />
        <img :src="h" alt="h" />
        <img :src="i" alt="i" />
        <img :src="j" alt="j" />
        <img :src="k" alt="k" />
        <img :src="l" alt="l" />
        <img :src="m" alt="m" />
      </div>
    </div>
  </section>
</template>
<style scoped>
.fans-grid {
  display: grid;
  grid-template-columns: repeat(6, 1fr); /* 6 columns */
  grid-template-rows: repeat(4, 1fr); /* 4 rows */
  gap: 10px; /* Add some space between grid items */
  width: 100%;
  height: 100vh; /* Full height for demonstration */
}
/* 
.grid-item {
  background-color: lightblue;
  display: flex;
  justify-content: center;
  align-items: center;
  border: 1px solid #ccc;
  font-size: 20px;
} */

.grid-item-1 {
  background: #000a2f;
  /* width: 100%;
  height: 100%; */
  grid-column: 1 / span 3; /* Start at column 1 and span 3 columns */
  grid-row: 1 / span 3;
}
</style>

<script setup>
import Button from "./Button.vue";
import a from "@/assets/fans/a.svg";
import b from "@/assets/fans/b.svg";
import c from "@/assets/fans/c.svg";
import d from "@/assets/fans/d.svg";
import e from "@/assets/fans/e.svg";
import f from "@/assets/fans/f.svg";
import g from "@/assets/fans/g.svg";
import h from "@/assets/fans/h.svg";
import i from "@/assets/fans/i.svg";
import j from "@/assets/fans/j.svg";
import k from "@/assets/fans/k.svg";
import l from "@/assets/fans/l.svg";
import m from "@/assets/fans/m.svg";
</script>
