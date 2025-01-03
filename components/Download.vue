<template>
  <section id="Download">
    <section id="Download" class="download-section px-16 py-16">
      <div class="download-container">
        <div class="download-image">
          <img :src="image" />
        </div>
        <div class="download-content">
          <p class="download-text">
            Get started with our team management app by downloading it today.
            Available on multiple platforms for seamless integration and user
            experience.
          </p>
          <div class="download-buttons">
            <a
              href="https://themewagon.github.io/pavo/#your-link"
              class="btn blue"
              >Download for iOS</a
            >
            <a
              href="https://themewagon.github.io/pavo/#your-link"
              class="btn pink"
              >Download for Android</a
            >
          </div>
        </div>
      </div>
    </section>
  </section>
  <section class="finalsec">
    <h5 class="head5">
      Pavo is a mobile application for marketing automation and you can reach
      the team at <span>email@domain.com</span>
    </h5>
    <div class="socialcontent">
      <a href=""><img class="social" :src="facebook" /></a>
      <a href=""><img class="social" :src="twitter" /></a>
      <a href=""><img class="social" :src="instagram" /></a>
      <a href=""><img class="social" :src="youtube" /></a>
      <a href=""><img class="social" :src="socialimg" /></a>
    </div>
    <div class="public px-4 py-4">
      <li>Article Details</li>
      <li>Terms and Conditions</li>
      <li>Privacy and Ploicy</li>
      <li>Copyright © Pavo</li>
      <li>Distributed by Themewagon</li>
    </div>
  </section>
</template>
<script setup>
import { image } from "~/assets/img/images";
import {
  facebook,
  twitter,
  instagram,
  youtube,
  socialimg,
} from "~/assets/img/images";
</script>
<style scoped>
/* Download Section */

.btn.blue {
  background-color: #0077cc;
}

.btn.pink {
  background-color: #e63946;
}
.download-section {
  display: flex;
  justify-content: center;
  padding: 4rem 4rem;
}

.download-container {
  display: flex;
  justify-content: space-between;
  align-items: center;
}

.download-image {
  flex: 1;
  padding-right: 3rem;
}

.download-content {
  flex: 1;
  padding-left: 2rem;
}

.head5 {
  color: #252c38;
  font-weight: 700;
  font-size: 1.5rem;
  line-height: 2rem;
  letter-spacing: -0.2px;
  text-align: center;
}
.download-buttons {
  margin-top: 2rem;
}
.btn:hover {
  opacity: 0.9;
}
.btn {
  display: inline-flex;
  padding: 1.375rem 2.25rem;
  border: 1px solid #594cda;
  border-radius: 2rem;
  background-color: #594cda;
  color: #ffffff;
  font-weight: 600;
  font-size: 1.1rem;
  text-decoration: none;
  transition: all 0.2s;
  flex: 1rem;
}

@media (max-width: 768px) {
  .download-container {
    flex-direction: column;
    width: 100%;
  }
  .btn {
    padding: 1rem 1.8rem;
    font-size: 1rem;
  }
  .download-content {
    padding: 0;
    width: 100%;
  }
  .download-section {
    padding: 0.8rem;
  }

  .download-image {
    margin-bottom: 1.5rem;
  }

  .download-buttons {
    display: flex;
    flex-direction: column;
    text-align: center;
    gap: 1.5rem;
    margin-top: 2rem;
  }

  .head5 {
    font-size: 0.9rem;
  }
  .public {
    font-size: 0.6rem;
  }
  .public {
    display: flex;
    flex-direction: column;
  }
}
.container {
  max-width: 75rem;
  margin: 0 auto;
  padding: 0 1.5rem;
}

.social {
  width: 2rem;
}
.socialcontent {
  margin-top: 2rem;
  line-height: 1.6;
  display: flex;
  gap: 1rem;
  justify-content: center;
}
.public {
  margin-top: 2rem;
  display: flex;
  align-items: center;
  justify-content: center;
  font-size: 0.8rem;
  gap: 2rem;
  list-style-type: none;
  color: black;
}
span {
  color: blue;
}
.image {
  width: 400rem;
}
.finalsec {
  background: linear-gradient(to top, #94c4f7, #e0f7ff);
  transition: background 0.5s ease;
  padding: 4rem;
}
</style>
