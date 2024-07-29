<template>
  <section id="trustedBrands" class="text-center w-full">
    <h1>
      Trusted by brands you trust.

      <div class="partners">
        <img :src="gt" alt="gt" />
        <img :src="printrite" alt="printrite" />

        <img :src="sie" alt="sie" />
      </div>
    </h1>
  </section>
</template>

<script setup>
import gt from "@/assets/gtco.svg";
import printrite from "@/assets/printrite.svg";
import sie from "@/assets/sie.svg";
</script>

<style scoped>
#trustedBrands {
  margin: 5rem 0;
  text-align: center;
}
#trustedBrands h1 {
  margin-bottom: 2rem;
}
.partners {
  display: flex;
  justify-content: center;
  align-items: center;

  padding: 2rem 0;
  width: 70%;
  margin: 0 auto;
  flex-wrap: wrap;
}
.partners img {
  width: 90px;
  /* aspect-ratio: 1/1; */
  height: 90px;
  margin: 0 3rem;

  object-fit: contain;
}

@media (max-width: 500px) {
  .partners {
    padding: 2rem 0;
    width: 90%;
  }
  .partners img {
    width: 70px;
    height: 70px;
  }
}
</style>
