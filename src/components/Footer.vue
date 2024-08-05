<template>
  <footer>
    <div class="container grid-container">
      <div>
        <img src="/myshelta.jpeg" class="logo" alt="myShelta" />
        <p>
          Shelta is a PropTech Startup that provides guaranteed rent for
          Landlords & flexible (monthly, biannual, quarterly) rent payment for
          tenants. Shelta takes away the friction between Landlord-Tenant
          relationships through our rent financing solution.
        </p>
      </div>

      <div class="grid-span-two">
        <h3>Company</h3>

        <ul>
          <li><a href="#">About</a></li>
          <li><a href="#">Safe</a></li>

          <li><a href="#">Rent Payer</a></li>
          <li><a href="#">Smart</a></li>
        </ul>
      </div>

      <div class="grid-span-two">
        <h3>Support</h3>

        <ul>
          <li><a href="#">FAQs</a></li>
          <li><a href="#">Contact Us</a></li>

          <li><a href="#">Register</a></li>
          <li><a href="#">Resources/Blog</a></li>
        </ul>
      </div>

      <div>
        <h3>Offices</h3>

        <p>
          4. Amurie Omanze, Off Samuel Ladoke Akintola Boulevard, Garki 2
          900001, Abuja, Federal Capital Territory.
        </p>

        <p>3. Abang Odok Close By AB Army Hotel, Mekenge Layout, Calabar.</p>

        <p>Opening hours: 9am - 5pm | Mon - Fri</p>
      </div>
    </div>
  </footer>

  <div class="copyright">
    <div class="container flex flex-between">
      <!-- LATER ON, CHANGE THE YEAR TO BE DYNAMIC -->
      <p>&copy; 2024, All rights reserved</p>

      <div class="flex footer-socials">
        <span>
          <img :src="facebook" alt="" />
        </span>
        <span>
          <img :src="instagram" alt="" />
        </span>
        <span>
          <img :src="twitter" alt="" />
        </span>
        <span>
          <img :src="linkedin" alt="" />
        </span>
      </div>
    </div>
  </div>
</template>

<style scoped>
footer {
  margin: 4rem 0;
  padding: 2rem 0;
}
.grid-container {
  width: 100%;
  display: grid;
  gap: 2rem;

  font-size: 1.3rem;
  line-height: 40px;
  grid-template-columns: repeat(4, 1fr);
  justify-content: center;
  /* align-items: center; */
}

.grid-span-two {
  /* grid-column: span 3; */
  grid-row: span 2;
}
.copyright {
  background: var(--primary);
  padding: 2rem 0;
  color: var(--secondary);
  /* margin-bottom: 0 !important; */
}

.footer-socials {
  gap: 1rem;
}

.copyright p {
  font-size: 1.2rem;
}

.copyright span {
  display: flex;
  align-content: center;
  border-radius: 50%;
  padding: 0.5rem;
  border: 1px solid var(--secondary);
}
.copyright img {
  color: var(--secondary);
  filter: invert(1);
}

@media (max-width: 800px) {
  .grid-container {
    gap: 3rem;
    justify-content: space-between;
    grid-template-columns: repeat(2, 1fr);
  }
}

@media (max-width: 600px) {
  .grid-container {
    grid-template-columns: 1fr;
    width: 100%;
  }
}
</style>

<script setup>
import facebook from "@/assets/facebook.png";
import linkedin from "@/assets/linkedin.png";
import twitter from "@/assets/twitter.png";
import instagram from "@/assets/instagram.png";
</script>
