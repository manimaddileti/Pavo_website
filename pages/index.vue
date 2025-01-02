<template>
  <Navbar />
  <HomePage />
</template>

<script setup>
import Navbar from "~/components/Navbar.vue";
import HomePage from "~/components/HomePage.vue";
useHead({
  title: "Pavo Webpage Title",
});
</script>


