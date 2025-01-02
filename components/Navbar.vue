<template>
  <header :class="['header', { scrolled: isScrolled }]">
    <nav class="navbar">
      <div class="logo">
        <a href="#Home"><img class="icon" :src="Pavoicon" /></a>
      </div>
      <div class="menu-toggle" @click="toggleMenu">&#9776;</div>
      <ul :class="['nav-links', { 'mobile-menu': isMenuOpen }]">
        <li><a href="#" class="link">Home</a></li>
        <li><a href="#Features" class="link">Features</a></li>
        <li><a href="#Details" class="link">Details</a></li>
        <li><a href="#Pricing" class="link">Pricing</a></li>
        <li class="dropdown">
          <a href="#Drop" class="link">Drop</a>
          <div class="dropdown-menu">
            <a href="" class="dropdown-link">Article Details</a>
            <a href="" class="dropdown-link">Terms and Conditions</a>
            <a href="" class="dropdown-link">Privacy Policy</a>
          </div>
        </li>
        <li><a href="#Download" class="link">Download</a></li>
        <li class="icons">
          <a href=""><img class="icons" :src="apple" /></a>
          <a href=""><img class="icons" :src="android" /></a>
        </li>
      </ul>
    </nav>
  </header>
</template>

<script setup>
import { apple, Pavoicon, android } from "~/assets/img/images";
import { ref, onMounted, onUnmounted } from "vue";
const isMenuOpen = ref(false);
const isScrolled = ref(false);
function toggleMenu() {
  isMenuOpen.value = !isMenuOpen.value;
}
function handleScroll() {
  isScrolled.value = window.scrollY > 0;
}
onMounted(() => {
  window.addEventListener("scroll", handleScroll);
});
onUnmounted(() => {
  window.removeEventListener("scroll", handleScroll);
});
</script>

<style scoped>
.header {
  background-color: skyblue;
  transition: background-color 0.3s ease, box-shadow 0.3s ease;
  padding: 1rem 4rem;
  position: fixed;
  left: 0;
  right: 0;
  top: 0;
  z-index: 1000;
}

.header.scrolled {
  background-color: white;
  box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
}

.navbar {
  display: flex;
  justify-content: space-between;
  align-items: center;
}

.logo img {
  width: 7rem;
  margin-left: 10px;
  transition: transform 0.3s ease;
}

.logo img:hover {
  transform: scale(1.1);
}

.nav-links {
  display: flex;
  list-style: none;
  gap: 1rem;
}

.link {
  text-decoration: none;
  color: #444;
  font-weight: bold;
  padding: 0.5rem;
  border-radius: 5px;
  transition: background-color 0.3s ease, color 0.3s ease;
}

.link:hover {
  color: orange;
}

.dropdown {
  position: relative;
}

.dropdown-menu {
  display: none;
  position: absolute;
  background: white;
  box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
  padding: 0.5rem;
  border-radius: 5px;
  top: 2rem;
  z-index: 1000;
}

.dropdown:hover .dropdown-menu {
  display: block;
}

.dropdown-link {
  display: block;
  padding: 0.5rem 1rem;
  color: #444;
  text-decoration: none;
  font-size: 0.9rem;
  transition: background 0.3s ease, color 0.3s ease;
}

.dropdown-link:hover {
  background: #0077cc;
  color: white;
}

.icons {
  display: flex;
  width: 50px;
  gap: 10px;
}

.menu-toggle {
  display: none;
  font-size: 2rem;
  cursor: pointer;
}

.nav-links,
.icons {
  margin-right: 20px;
}

@media (max-width: 768px) {
  .nav-links {
    display: none;
    flex-direction: column;
    gap: 0;
    position: absolute;
    top: 100%;
    left: 0;
    width: 100%;
    background-color: skyblue;
    box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
  }

  .mobile-menu {
    display: flex;
  }

  .menu-toggle {
    display: block;
  }

  .link {
    text-align: center;
    padding: 1rem;
  }

  .dropdown-menu {
    position: static;
    box-shadow: none;
    background: transparent;
  }

  .dropdown-link {
    padding: 0.5rem;
  }
}
</style>
