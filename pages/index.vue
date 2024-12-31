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

<style scoped>
body {
  font-family: Arial, sans-serif;
  margin: 0;
  padding: 0;
  background-color: skyblue;
}

.container {
  width: 100%;
  max-width: 1200px;
  margin: 0 auto;
  padding: 0 20px;
  background: white;
}

.header {
  background: linear-gradient(to right, #cce7ff, #fde2e4);
  padding: 1rem 2rem;
  box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
}

.app {
  display: flex;
  align-items: center;
  justify-content: space-between;
  padding: 4rem 0;
}

.app-text {
  max-width: 50%;
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
  gap: 2rem;
}

.btn {
  padding: 0.75rem 1.5rem;
  border: none;
  border-radius: 5px;
  color: white;
  cursor: pointer;
  font-size: 1rem;
  text-decoration: none;
  text-align: center;
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
}

.features-section {
  padding: 4rem 0;
  text-align: center;
  background-color: #f5f8fa;
}

.features-section h1 {
  font-size: 2rem;
  margin-bottom: 2rem;
  color: #333;
}

.features-container {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 1.5rem;
  margin: 0 auto;
  max-width: 1200px;
}

.feature-box {
  background: white;
  padding: 1.5rem;
  border-radius: 10px;
  box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
  transition: transform 0.3s ease, box-shadow 0.3s ease;
}

.feature-box:hover {
  transform: translateY(-5px);
  box-shadow: 0 6px 10px rgba(0, 0, 0, 0.15);
}

.feature-box h2 {
  font-size: 1.2rem;
  color: #0077cc;
  margin-bottom: 0.8rem;
}

.feature-box p {
  font-size: 0.9rem;
  color: #555;
  line-height: 1.5;
}

.kkk {
  font-size: 30px;
}

.details-section {
  padding: 2rem 0;
  text-align: center;
}

.details-section h1 {
  font-size: 2rem;
  color: #333;
  margin-bottom: 1.5rem;
}

.details-images {
  display: flex;
  justify-content: center;
  gap: 1.5rem;
}

.details-images img {
  max-width: 45%;
  border-radius: 8px;
  box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
}
</style>
