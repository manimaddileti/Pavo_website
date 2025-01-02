<script lang="ts" setup>
import { detailsImage1 } from "~/assets/img/images";
import { detailsImage2 } from "~/assets/img/images";
import { detailsImage3 } from "~/assets/img/images";
</script>
<template>
  <div class="flex flex-col justify-between  p-4 lg:p-20">
    <div class="grid grid-cols-1 lg:grid-cols-2 gap-10">
      <div class="flex flex-col justify-center items-center">
        <h2>Results driven ground breaking technology</h2>
        <p>
            Based on our team's extensive experience in developing line of business applications and constructive customer feedback we reached a new level of revenue.
        </p>

        <p>
            We enjoy helping small and medium sized tech businesses take a shot at established Fortune 500 companies
        </p>
      </div>

      <div class="details-images">
        <img :src="detailsImage1" />
      </div>
    </div>

    <div class="grid grid-cols-1 lg:grid-cols-2 gap-10">
      <div class="details-images">
        <img :src="detailsImage2" />
      </div>
      <div class="flex flex-col justify-center  items-center">
        <h2>Results driven ground breaking technology</h2>
        <p>
          Based on our team's extensive experience in developing line of
          business applications and constructive customer feedback we reached a
          new level of revenue.
        </p>

        <p>
            Features that will help you and your marketers,
            mooth learning curve due to the knowledge base,
            Ready out-of-the-box with minor setup settings.
        </p>
      </div>
    </div>

    <div class="grid grid-cols-1 lg:grid-cols-2 gap-10">
      <div class="flex flex-col justify-center items-center">
        <h2>Results driven ground breaking technology</h2>
        <p>
            Get a glimpse of what this app can do for your marketing automation and understand why current users are so excited when using Pavo together with their teams.
        </p>

        <p>
            We will promptly answer any questions and honor your requests based on the service level agreement
        </p>
      </div>

      <div class="details-images">
        <img :src="detailsImage3" />
      </div>
    </div>
  </div>
</template>

<style scoped>
p {
  color: #6b747b;
  font: 400 1rem/1.625rem "Open Sans", sans-serif;
  margin-bottom: 1rem;
}
h2 {
  color: #252c38;
  font-weight: 700;
  font-size: 2.125rem;
  line-height: 2.625rem;
  letter-spacing: -0.4px;
  margin-bottom: 1.5rem;
}
</style>
