<template>
  <section class="app px-16 py-16">
    <div class="app-text">
      <h1><strong>Team management mobile application</strong></h1>
      <p>
        Start getting things done together with your team based on Pavo's
        revolutionary team management features.
      </p>
      <div class="buttons">
        <a href="" class="btn blue">Download</a>
        <a href="" class="btn pink">Download</a>
      </div>
    </div>

    <div class="app-image">
      <img :src="headerSmartphone" alt="Team management mobile app" />
    </div>
  </section>

  <section class="paragraph">
    <p class="kkk font-light">
      Team management mobile apps don’t get better than Pavo. It’s probably the
      best app in the world for this purpose. Don’t hesitate to give it a try
      today and you will fall in love with it.
    </p>
  </section>
  <Features />
  <Details />
  <Pricing />
  <Download />
</template>

<script setup>
import { headerSmartphone } from "~/assets/img/images";
import Features from "./Features.vue";
import Details from "./Details.vue";
import Pricing from "./Pricing.vue";
import Download from "./Download.vue";
</script>

<style scoped>
.app {
  display: flex;
  align-items: center;
  justify-content: space-between;
  padding: 4rem 4rem;
  background: linear-gradient(to top, white, lightskyblue);
  transition: background 0.5s ease;
}
.kkk {
  text-align: center;
  font-size: 30px;
  padding: 4rem;
}

.app-text {
  max-width: 40%;
  margin-top: 5rem;
}

.app-text h1 {
  font-size: 2.5rem;
  color: #333;
  margin-bottom: 1rem;
}

.app-text p {
  font-size: 1rem;
  color: #555;
  margin-bottom: 2rem;
}

.buttons {
  display: flex;
  gap: 1rem;
}

.btn {
  display: inline-block;
  padding: 1.375rem 2.25rem;
  border: 1px solid #594cda;
  border-radius: 32px;
  background-color: #594cda;
  color: #ffffff;
  font-weight: 600;
  font-size: 0.875rem;
  text-decoration: none;
  transition: all 0.2s;
}

.btn.blue {
  background-color: #0077cc;
}

.btn.pink {
  background-color: #e63946;
}

.btn:hover {
  opacity: 0.9;
}

.app-image img {
  max-width: 100%;
  height: auto;
  margin-right: 100px;
}

@media (max-width: 768px) {
  .app {
    flex-direction: column;
    text-align: center;
    padding: 2rem 1rem;
  }
  
  p.kkk {
    text-align: left;
    font-size: 2rem;
    width: 100%;
    padding:0.5rem;
  }
  .app-text {
    max-width: 100%;
  }

  .app-text h1 {
    font-size: 1.8rem;
  }

  .app-text p {
    font-size: 0.9rem;
  }

  .buttons {
    flex-direction: column;
    gap: 0.8rem;
  }

  .app-image {
    margin-top: 2rem;
  }

  .btn {
    padding: 1rem 1.8rem;
    font-size: 1rem;
  }
}
</style>
