<template>
    <header class="header">
      <nav class="navbar">
        <div class="logo">
          <a href="index.html">
            <img class="icon" src="https://themewagon.github.io/pavo/images/logo.svg" alt="Pavo Logo" />
          </a>
        </div>
        <ul class="nav-links">
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
          <i class="fab fa-apple text-indigo-600 hover:text-pink-500 text-xl transition-all duration-200 mr-1.5"></i>
          <i class="fab fa-google text-indigo-600 hover:text-pink-500 text-xl transition-all duration-200 mr-1.5"></i>
        </ul>
      </nav>
    </header>
  </template>
  
  <script setup>
  </script>
  
  <style scoped>
  .header {
    background: linear-gradient(to right, #cce7ff, #fde2e4);
    padding: 1rem 2rem;
    box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
    position: fixed;
    left: 0;
    right: 0;
    top: 0;
  }
  
  .navbar {
    display: flex;
    justify-content: space-between;
    align-items: center;
    
  }
  
  .logo img {
    width: 7rem;
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
  </style>
  