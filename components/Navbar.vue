<template>
  <header class="header">
    <nav class="navbar">
      <div class="logo">
        <a href="#Home">
          <img
            class="icon"
            src="https://themewagon.github.io/pavo/images/logo.svg"
            alt="Pavo Logo"
          />
        </a>
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
          <a href=""
            ><img
              class="icons"
              src="data:image/png;base64,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"
          /></a>
          <a href=""
            ><img
              class="icons"
              src="data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAAJwAAACUCAMAAABRNbASAAAAWlBMVEX///+m2GT3+/Kj116o2Wnb78Pl89X2+++e1VGf1VXv+OXX7b3+//yl12Gh1lr7/fnK56e54Iiv3HW74Y3e8Mmz3n7i8s/B45fs9t+r2m7O6a7G5qDT67a23oKiMR2RAAAEvUlEQVR4nO2ca9eyKhCGE0hEg8xD2un//81tJclBTXsY17vWnvtbGXE1nAaYabdbpWN2KbLjujK6ZHH5reRiXYWUovylZPkseQ3NY4pHMooiVZK1BUmpuoIy4hBUvdJnFU+6w7pyh7IvmMJwvURq2tOt6j3Hno3Wq02+Rq2U6+k0m5QtHNlTsZJjLUvafX5rytOpbG75vrUMpNtUqhiWraOLerpTT0DifRmJRChFqZSUKtW9iMp9rJ+ferYInK2jS7Ttnq/SvJaCvt8xJKmQdf7q/tpuyQZspu3S6pEoD+wDqJJHlW5pt6fa3na0UHSK7C2qCtrbDXgsDIqZ7M3xVf0H2UZ2e9FNN+Z4A2/I9ux3q7Qp2+6+Du6+IRrvp4fFUiXkim8pZSvZOjoGueQbatmXCWRMlG0yl+gVYqU2WSFa9hPbc64Dt13qr6OL6ShwvzvWP/Q3LVXDbnBu9jiVX8zoPFc3SLZKWHUpJsUMXveQKevXiAqOjZhLvVR5ynlVTLYzLSrO09xchmUEt4loDBDJzq/3juUEHe23GWdzeFOwhm3NJqR6veTjHU9SvWLdTXqwPY41UtmngfLRxUzl+jlh5m+qYdjSxLTAUMl+HG4//CjTtAnMZNdYzVMMcKOdjg5whdUdGgi2llmVs48TdBuH+3R97hSE6HVXu/Wo7lPphP/0ORfJbXgFcdRUOIOyH67p1ERHizfd3XludIhgahOncknLM2/zaSdFsrzl59LzFAB2iSMTBk2SZNYnVt0HfLsOk0ww1T+7Sq5k8KkuvYRii6JL6KnuHMxwnenOgeGy1RuuaaksMFz+Bw/YFQ08IiYdo5/g1p0of4d7hIR7hIUj7vrwF8kirD9Mft2tjsKxwHBKBJQKvJPgQRWWDYX6H4ukccuti7dDHFT2d/M2TpdOLlVDRSLEybyRJyIJKGGgHLOT6KqjzZIzHt6ot9dPxWNw9km49eGpAa59iNeqLalqvk5/aTQ4bnQ4sSJLrpKWyjhrqsTgUKjoi4fMrfMQGWnbAcG11tfSet52jbNz1v4DDBxx9rxq9qjC272LDBIuE86T2eiJmwunt+cwcJ6TOHto7LuU/fE8CFzqedeymA5YIf7mlMZwcLHv+rPpIZEy79P9MRsI3MjB3sz9HcIhHMIhHMIhHMIhHMIhHMIhHMIhHMIhHMIhHMIhHMIhHMIhHMIhHMJtAMdH4M5wcOdVV5qHi38Z3MLBtf5l8GXm3wv8sFF2gIM7eA1F5/6WInaj43UcOcwdvxfvPpuP6CbESR2HAgOXOt9K69n/pHDSHD+JNEBBL3b6ztdUybOZIJoMGUhA4UK50Y9k8jVmPS76FDdJjVRoKLjdPeqTOaQqFiTA8pwlQolENoaRweB2bSNf1bF8WQwsie/5tbKi++DgdgdeXfN7TFyK5SL+9PwHuEvYIObjKWTg/ClwEu4/naxBLsFMRwO3aif+9f8/FqKpAiA0nWS1DnkdqVOZ0axjXUAHutYZTHLw4fgWGclPy/TDTodsJBON6IcgaAakG83o9vGR0SOgoWbgqA3nWw7hEA7hEA7hEA7hEA7hEA7htobDPcQy+YZRVo5lNfKBrdh2flI/tQ4l/QsGyX6p5z9ESm3T7gi9QQAAAABJRU5ErkJggg=="
          /></a>
        </li>
      </ul>
    </nav>
  </header>
</template>

<script setup>
import { ref } from "vue";
const isMenuOpen = ref(false);

const toggleMenu = () => {
  isMenuOpen.value = !isMenuOpen.value;
};
</script>

<style scoped>
.header {
  background: linear-gradient(to right, #cce7ff, #fde2e4);
  padding: 1rem 4rem;
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

/* Responsive Styles */
@media (max-width: 768px) {
  .nav-links {
    display: none;
    flex-direction: column;
    gap: 0;
    position: absolute;
    top: 100%;
    left: 0;
    width: 100%;
    background: linear-gradient(to right, #cce7ff, #fde2e4);
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
