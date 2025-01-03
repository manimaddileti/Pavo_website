<template>
  <section id="Features" class="py-16 bg-white text-center">
    <div
      class="max-w-7xl mx-auto grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-3 gap-8 px-4"
    >
      <div
        class="bg-sky-100 p-6 rounded-lg shadow-md hover:shadow-lg hover:scale-105 transition-all"
      >
        <img
          :src="featureIcon1"
          alt="Platform Integration Icon"
          class="w-16 h-16 mx-auto mb-4"
        />
        <h2 class="text-lg font-semibold mb-2">Platform Integration</h2>
        <p class="text-sm text-gray-700">
          Your sales force can use the app on any smartphone platform without
          compatibility issues.
        </p>
      </div>

      <div
        class="bg-sky-100 p-6 rounded-lg shadow-md hover:shadow-lg hover:scale-105 transition-all"
      >
        <img
          :src="featureIcon2"
          alt="Easy On Resources Icon"
          class="w-16 h-16 mx-auto mb-4"
        />
        <h2 class="text-lg font-semibold mb-2">Easy On Resources</h2>
        <p class="text-sm text-gray-700">
          Works smoothly even on older generation hardware due to our
          optimization efforts.
        </p>
      </div>

      <div
        class="bg-sky-100 p-6 rounded-lg shadow-md hover:shadow-lg hover:scale-105 transition-all"
      >
        <img
          :src="featureIcon3"
          alt="Great Performance Icon"
          class="w-16 h-16 mx-auto mb-4"
        />
        <h2 class="text-lg font-semibold mb-2">Great Performance</h2>
        <p class="text-sm text-gray-700">
          Optimized code and innovative technology ensure no delays and
          ultra-fast responsiveness.
        </p>
      </div>

      <div
        class="bg-sky-100 p-6 rounded-lg shadow-md hover:shadow-lg hover:scale-105 transition-all"
      >
        <img
          :src="featureIcon4"
          alt="Multiple Languages Icon"
          class="w-16 h-16 mx-auto mb-4"
        />
        <h2 class="text-lg font-semibold mb-2">Multiple Languages</h2>
        <p class="text-sm text-gray-700">
          Choose from one of the 40 languages that come pre-installed and start
          selling smarter.
        </p>
      </div>

      <div
        class="bg-sky-100 p-6 rounded-lg shadow-md hover:shadow-lg hover:scale-105 transition-all"
      >
        <img
          :src="featureIcon5"
          alt="Free Updates Icon"
          class="w-16 h-16 mx-auto mb-4"
        />
        <h2 class="text-lg font-semibold mb-2">Free Updates</h2>
        <p class="text-sm text-gray-700">
          Don't worry about future costs, pay once and receive all future
          updates at no extra cost.
        </p>
      </div>

      <div
        class="bg-sky-100 p-6 rounded-lg shadow-md hover:shadow-lg hover:scale-105 transition-all"
      >
        <img
          :src="featureIcon6"
          alt="Community Support Icon"
          class="w-16 h-16 mx-auto mb-4"
        />
        <h2 class="text-lg font-semibold mb-2">Community Support</h2>
        <p class="text-sm text-gray-700">
          Register the app and get access to knowledge and ideas from the Pavo
          online community.
        </p>
      </div>
    </div>
  </section>
</template>

<script setup>
import {
  featureIcon1,
  featureIcon2,
  featureIcon3,
  featureIcon4,
  featureIcon5,
  featureIcon6,
} from "~/assets/img/images";
</script>
