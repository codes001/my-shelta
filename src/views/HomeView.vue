<script setup>
import HomeHero from "../components/HomeHero.vue";
import Header from "@/components/Header.vue";
import Navbar from "@/components/Navbar.vue";
import TrustedBrands from "@/components/TrustedBrands.vue";
import a from "@/assets/pmicon.svg";
import b from "@/assets/fmicon.svg";
import c from "@/assets/cicon.svg";
</script>

<template>
  <main>
    <Header />
    <Navbar />
    <HomeHero />

    <section class="property-financing w-full">
      <div class="container flex props-finance-container">
        <div class="property-financing-one">
          <h4 class="text-primary uppercase">property financing</h4>
          <h1>Everything you need to get paid on time</h1>
        </div>
        <div class="property-financing-two flex flex-col">
          <!-- <p>
            
          </p> -->
          <p>
            Living in your desired environment or getting your dream house
            should not be difficult. <br />
            <br />
            <br />
            With SAFE flexible payment by Shelta, you can rent or buy properties
            in any location of your choice and also benefits from our renewable
            energy solutions that takes care of your lightning needs.
          </p>
        </div>
      </div>
    </section>

    <section class="sub-financing flex">
      <div class="flex" style="gap: 1rem">
        <span class="num-one">1.</span>
        <p>Rent Financing</p>
      </div>

      <div class="flex" style="gap: 1rem">
        <span class="num-two">2.</span>
        <p>Property Financing</p>
      </div>

      <div class="flex" style="gap: 1rem">
        <span class="num-three">3.</span>
        <p>Renewable Energy</p>
      </div>
    </section>

    <!-- PROPERTY MANAGEMENT -->
    <section class="w-full">
      <div class="container props-management">
        <!-- CHILD 1 -->
        <div class="props-management-one">
          <h4 class="text-primary uppercase">property management</h4>
          <h1 class="font-bold">
            Everything you need to enjoy sustainable living
          </h1>

          <p>
            As a landlord, you should not wait to get your deserved rent nor beg
            to handle your properties with care. Shelta SAFE product offers a
            simple and secure way for landlords to get paid without delay. Also,
            we manage your properties that it retains its value and protect you
            and yours from any act of legal claim from tenants.
          </p>
        </div>

        <!-- CHILD 2 -->
        <div class="props-child-two">
          <div class="pm">
            <img :src="a" alt="pm" />
            <p>Property Management</p>
          </div>

          <div class="fm">
            <img :src="b" alt="pm" />
            <p>Facility Management</p>
          </div>

          <div class="lc">
            <img :src="c" alt="pm" />
            <p>Litigation Cover</p>
          </div>
        </div>
      </div>
    </section>

    <TrustedBrands />
  </main>
</template>

<style scoped>
main {
  padding-bottom: 5rem;
}
.property-financing {
  width: 100%;

  gap: 2rem;
  margin: 4rem 0;
}

.property-financing .property-financing-one {
  width: 50%;
}

.property-financing .property-financing-two {
  width: 50%;
  gap: 2rem;
  font-weight: 400;
  /* flex: 50% 50%; */
}
.props-finance-container {
  gap: 2rem;
}

.sub-financing {
  justify-content: space-evenly;
  padding: 2rem 0;
  margin: 2rem 0;
  color: #333;
}

.props-management {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 4rem;
}
.props-management .props-management-one p {
  font-size: 0.9rem;

  font-weight: normal;
}

.props-management .props-child-two {
  display: grid;

  grid-template-columns: repeat(3, 1fr);
  justify-content: center;
  align-items: center;
  /* text-align: center; */
  gap: 2rem;
}

.props-management .props-child-two div {
  width: 150px;
  height: 150px;
  padding: 1rem;
  border-radius: 10px;
  display: flex;
  flex-direction: column;
  gap: 1rem;
  align-items: end;
}

.props-management .props-child-two div img {
  width: 40px;
  height: 40px;
  border-radius: 50%;
}

.pm {
  background: #f1ccfb;
}
.fm {
  background: #fbf1cc;
  transform: translateY(50px);
}
.lc {
  background: #ccfbd9;
}
/* MEDIA QUERIES */
@media (max-width: 500px) {
  .props-finance-container {
    flex-direction: column;
    width: 100%;
  }

  .property-financing .property-financing-one,
  .property-financing .property-financing-two {
    width: 95%;
    /* padding: 0 10px; */
  }
  .sub-financing {
    flex-direction: column;
    padding: 2rem 0;
    gap: 1rem;
    padding: 1.2rem;
    align-items: start;
  }
}
</style>
