<template>
  <div class="slider-container">
    <div class="slider">
      <div
        v-for="(slide, index) in slides"
        :key="index"
        :class="{ slide: true, active: currentSlide === index }"
      >
        <img :src="slide.image" :alt="slide.reviewer" />
        <div class="review-content">
          <p class="review-text">"{{ slide.review }}"</p>
          <p class="reviewer-name">- {{ slide.reviewer }}</p>
          <span> {{ slide.userType }} </span>
        </div>
      </div>
    </div>
    <div class="navigation">
      <button @click="prevSlide">
        <img :src="arrowLeft" alt="" style="filter: invert(1); width: 30px" />
      </button>
      <button @click="nextSlide">
        <img :src="arrowRight" alt="" style="filter: invert(1); width: 30px" />
      </button>
    </div>
  </div>
</template>

<script setup>
import { ref } from "vue";
import arrowLeft from "@/assets/arrow-left.png";
import arrowRight from "@/assets/arrow-right.png";

// Sample slides data
const slides = ref([
  {
    image:
      "https://ik.imagekit.io/9ioq0auj1/landlord1.svg?updatedAt=1723095194362",
    review:
      "I wish I would have thought of it first. Shelta is the next big property management company.",
    reviewer: "Adedayo E.",
    userType: "Landlord",
  },
  {
    image:
      "https://ik.imagekit.io/9ioq0auj1/tenant1.svg?updatedAt=1723095396802",
    review:
      "Seriously, Shelta was my saver in times of need.  Beyond their quick response, I am happy with the flexibility payment because it takes a whole lot of financial burden on myself. Thank you, Shelta.",
    reviewer: "Eliana M.",
    userType: "Tenant",
  },
]);

const currentSlide = ref(0);

function nextSlide() {
  currentSlide.value = (currentSlide.value + 1) % slides.value.length;
}

function prevSlide() {
  currentSlide.value =
    (currentSlide.value - 1 + slides.value.length) % slides.value.length;
}

function goToSlide(index) {
  currentSlide.value = index;
}
</script>

<style scoped>
.slider-container {
  position: relative;
  width: 80%;
  height: 500px;
  margin: 3rem auto auto;
}

.slider {
  display: flex;
  overflow: hidden;
  width: 100%;
  /* height: 500px; */
  padding: 0 2rem;
  position: relative;
}

.slide {
  min-width: 100%;
  transition: transform 0.5s ease;
  opacity: 0;
  position: absolute;
  top: 0;
  left: 0;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
}

.slide.active {
  opacity: 1;
  position: relative;
  z-index: 1;
}

.slide img {
  width: 100%;
  height: 400px;
  object-fit: contain;
}

.review-content {
  color: #333;
  text-align: center;
  padding: 20px;
  width: 100%;
}

.review-text {
  font-size: 1rem;
  margin: 0;
  text-align: justify;
}

.reviewer-name {
  font-size: 1.2rem;
  margin-top: 10px;
  font-weight: 700;
}

.navigation {
  display: flex;
  justify-content: flex-end;
  gap: 2rem;
  position: absolute;
  width: 100%;
  top: 0;
  right: 0;
  /* transform: translateY(-50%); */
  z-index: 2;
}

.navigation button {
  background: #0033ea;
  border: none;
  color: white;
  padding: 10px;
  cursor: pointer;
}

@media (min-width: 1000px) {
  .slide {
    flex-direction: row;
  }

  .slider-container {
    height: max-content;
    margin-bottom: 6rem;
  }

  .slide img {
    width: 100%;
    height: auto;
    object-fit: cover;
  }
  .review-text {
    text-align: center;
    font-size: 1.5rem;
  }
}

@media (max-width: 600px) {
  .slider-container {
    min-width: 100%;
    margin-bottom: 19rem;
  }

  .navigation {
    width: 100%;
    position: static;
    justify-content: center;
    gap: 2rem;
    margin-top: 3rem;
    z-index: 2;
  }

  .review-content {
    padding: 0;
  }
}
</style>
