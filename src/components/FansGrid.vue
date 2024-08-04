<template>
  <section class="w-full">
    <div class="container fans-grid">
      <div class="fans-grid-main">
        <div class="grid-item flex-col grid-item-1 text-center">
          <h2 class="text-center">Loved by 10,000+ Africans</h2>

          <hr style="width: 100px; text-align: center" />

          <Button label="Create a free account" type="button" />
        </div>

        <img class="" :src="a" alt="a" />
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
        <img :src="l" alt="l" />
        <img :src="m" alt="m" />
      </div>
    </div>
  </section>
</template>
<style scoped>
.fans-grid {
  gap: 0;
}

.fans-grid img {
  width: 200px;
  height: 200px;
}
.fans-grid-main {
  display: grid;
  grid-template-columns: repeat(7, 1fr);
  grid-template-rows: repeat(4, 1fr);
  gap: 10px;
  width: 100%;
  overflow-x: hidden;
  height: 100vh;
}

.grid-item-1 {
  background: #000a2f;
  border-radius: 10px;
  grid-column: span 3;
  grid-row: span 2;
  justify-content: center;
  align-items: center;
  color: #fff;
  gap: 1rem;
}

.grid-item-1 h2 {
  font-size: 2rem;
}

@media (max-width: 1100px) {
  .fans-grid-main {
    grid-template-columns: repeat(5, 1fr);
  }
}

@media (max-width: 900px) {
  .fans-grid img {
    width: 150px;
    height: 150px;
  }
  .fans-grid-main {
    grid-template-columns: repeat(4, 1fr);
  }
}

@media (max-width: 768px) {
  .fans-grid img {
    display: none;
  }

  .grid-item-1 {
    background: #000a2f;
    width: 100% !important;
    /* grid-column: 1fr;
    grid-row: 1fr; */
    height: 400px;
    color: #fff;
    gap: 1rem;
  }

  .fans-grid-main {
    display: grid;
    grid-template-columns: 1fr;
    gap: 10px;
    width: 100%;
  }
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
