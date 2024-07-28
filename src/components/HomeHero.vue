<template>
  <section class="home-hero">
    <div class="container">
      <div class="home-hero-text flex-col">
        <h2>Property Financing and Management for Every African</h2>
        <p>
          Shelta makes living sustainable, accessible, peacefull and rewarding
          for all.
        </p>

        <div class="home-hero-btn">
          <Button label="Create a free account" type="button" />
          <WhiteButton label="Contact Sales" type="button" />
        </div>
      </div>
      <div class="home-hero-img">
        <img src="/src/assets/firsthero.svg" alt="" />
      </div>
    </div>
  </section>
</template>

<style scoped>
.home-hero {
  height: 600px;
  padding: 1rem 0.5rem;
  width: 100%;
  background-color: #f8f9fa;
}

.home-hero > div {
  width: 100%;

  display: flex;
  gap: 2.5rem;
  padding: 30px 20px;
}

.home-hero-text {
  width: 50%;
}

.home-hero-text h2 {
  font-size: 35px;
  font-weight: 600;
  margin-bottom: 1rem;
}

.home-hero-img {
  width: 500px;
  height: 500px;
  aspect-ratio: 1/1;
}

.home-hero-img img {
  width: 100%;
  height: 100%;
}

.home-hero-btn {
  display: flex;
  gap: 1rem;
  margin-top: 1rem;
}

@media (max-width: 768px) {
  .home-hero-img {
    width: 400px;
    height: 400px;
  }
  .home-hero-btn button {
    font-size: 0.7rem;
  }
}

@media (max-width: 500px) {
  .home-hero {
    background-image: linear-gradient(
        rgba(195, 203, 209, 0.75),
        rgba(225, 227, 244, 0.322)
      ),
      url("/src/assets/firsthero.svg");
  }

  .home-hero img {
    display: none;
  }

  .home-hero-text {
    width: 100% !important;
    /* text-align: ; */
    padding: 0;
  }

  .home-hero > div {
    width: 100% !important;
    flex-wrap: wrap;
    margin-top: 5rem;
  }

  .home-hero-text h2 {
    font-size: 30px;
    margin-bottom: 2rem;
  }

  .home-hero-btn button {
    font-size: 0.8rem;
  }
}
</style>

<script setup>
import Button from "@/components/Button.vue";
import WhiteButton from "@/components/WhiteButton.vue";
</script>
