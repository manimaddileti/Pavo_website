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
    <p class="kkk">
      Team management mobile apps don’t get better than Pavo. It’s probably the
      best app in the world for this purpose. Don’t hesitate to give it a try
      today and you will fall in love with it.
    </p>
  </section>
  <section id="Features" class="features-section px-16 py-16">
    <h1 class="features-heading">Features</h1>
    <div class="features-container">
      <div class="feature-box">
        <img :src="featureIcon1" />
        <h2>Platform Integration</h2>
        <p>
          Your sales force can use the app on any smartphone platform without
          compatibility issues.
        </p>
      </div>
      <div class="feature-box">
        <img :src="featureIcon2" />
        <h2>Easy On Resources</h2>
        <p>
          Works smoothly even on older generation hardware due to our
          optimization efforts.
        </p>
      </div>
      <div class="feature-box">
        <img :src="featureIcon3" />
        <h2>Great Performance</h2>
        <p>
          Optimized code and innovative technology ensure no delays and
          ultra-fast responsiveness.
        </p>
      </div>
      <div class="feature-box">
        <img :src="featureIcon4" />
        <h2>Multiple Languages</h2>
        <p>
          Choose from one of the 40 languages that come pre-installed and start
          selling smarter.
        </p>
      </div>
      <div class="feature-box">
        <img :src="featureIcon5" />
        <h2>Free Updates</h2>
        <p>
          Don't worry about future costs, pay once and receive all future
          updates at no extra cost.
        </p>
      </div>
      <div class="feature-box">
        <img :src="featureIcon6" />
        <h2>Community Support</h2>
        <p>
          Register the app and get access to knowledge and ideas from the Pavo
          online community.
        </p>
      </div>
    </div>
  </section>
  <Details />
  <section>
    <div class="statistics-container">
      <div class="stat-box">
        <h2>231</h2>
        <p>Happy Users</p>
      </div>
      <div class="stat-box">
        <h2>385</h2>
        <p>Issues Solved</p>
      </div>
      <div class="stat-box">
        <h2>159</h2>
        <p>Good Reviews</p>
      </div>
      <div class="stat-box">
        <h2>127</h2>
        <p>Case Studies</p>
      </div>
      <div class="stat-box">
        <h2>211</h2>
        <p>Orders Received</p>
      </div>
    </div>

    <div class="py-10 mt-10">
      <h2 class="text-2xl font-bold text-center text-gray-800 mb-8">
        What do users think about Pavo
      </h2>
      <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8">
        <div
          v-for="users in userlist"
          :key="users.name"
          class="bg-blue-50 p-6 rounded-lg shadow"
        >
          <img
            :src="users.image"
            alt="User photo"
            class="mx-auto rounded-full w-20 h-20 mb-4"
          />
          <p class="italic text-gray-600 mb-4">"{{ users.text }}"</p>
          <h3 class="font-bold text-gray-800">
            {{ userlist.name }} - {{ userlist.role }}
          </h3>
        </div>
      </div>
    </div>
  </section>

  <section id="Pricing">
    <h1 class="pricing-heading px-16 py-16">Pricing options for all budgets</h1>
    <p class="par">
      Our pricing plans are setup in such a way that any user can start enjoying
      Pavo without worrying so much about costs.<br />
      They are flexible and work for any type of industry
    </p>
    <div class="pricing-container">
      <div class="pricing-box">
        <h2 class="head1">STANDARD</h2>
        <p class="price">$29 <span>/ month</span></p>
        <p>This basic package covers the marketing needs of small startups:</p>
        <ul>
          <li>List building and relations</li>
          <li>Seamless platform integration</li>
          <li>Great performance on devices</li>
          <li>Community support and videos</li>
        </ul>
        <a href="#" class="btn blue">Download</a>
      </div>

      <div class="pricing-box">
        <h2 class="head1">ADVANCED</h2>
        <p class="price">$39 <span>/ month</span></p>
        <p>This is a more advanced package suited for medium companies:</p>
        <ul>
          <li>List building and relations</li>
          <li>Seamless platform integration</li>
          <li>Great performance on devices</li>
          <li>Community support and videos</li>
        </ul>
        <a href="#" class="btn blue">Download</a>
      </div>

      <div class="pricing-box">
        <h2 class="head1">COMPLETE</h2>
        <p class="price">$49 <span>/ month</span></p>
        <p>This is a comprehensive package designed for big organizations:</p>
        <ul>
          <li>List building and relations</li>
          <li>Seamless platform integration</li>
          <li>Great performance on devices</li>
          <li>Community support and videos</li>
        </ul>
        <a href="#" class="btn blue">Download</a>
      </div>
    </div>
  </section>

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
      the team at <span>mvmkr2334@gmail.com</span>
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
      <li>Copyright © MVMKR</li>
      <li>Distributed by VHypotenuse</li>
    </div>
  </section>
</template>

<script setup>
import { headerSmartphone } from "~/assets/img/images";
import {
  featureIcon1,
  featureIcon2,
  featureIcon3,
  featureIcon4,
  featureIcon5,
  featureIcon6,
} from "~/assets/img/images";
import {
  detailsImage1,
  detailsImage2,
  detailsImage3,
} from "~/assets/img/images";
import {
  image,
  facebook,
  twitter,
  instagram,
  youtube,
  socialimg,
} from "~/assets/img/images";
import Details from "./Details.vue";

const userlist = [
  {
    image: "https://themewagon.github.io/pavo/images/testimonial-4.jpg",
    text: "We've been waiting for a powerful piece of software that can help businesses manage their marketing projects",
    name: "Tim Shaw",
    role: "Designer",
  },
  {
    image: "https://themewagon.github.io/pavo/images/testimonial-5.jpg",
    text: "Searching for a great prototyping and layout design app was difficult but thankfully I found app suite quickly",
    name: "Lindsay Spice",
    role: "Marketer",
  },
  {
    image: "https://themewagon.github.io/pavo/images/testimonial-6.jpg",
    text: "The app support team is amazing. They've helped me with some issues and I am so grateful to the entire team",
    name: "Ann Blake",
    role: "Developer",
  },
  {
    image: "https://themewagon.github.io/pavo/images/testimonial-1.jpg",
    text: "It's been so fun to work with Pavo, I've managed to integrate it properly into my business flow and it's great",
    name: "Jude Thorn",
    role: "Designer",
  },
  {
    image: "https://themewagon.github.io/pavo/images/testimonial-2.jpg",
    text: "We were so focused on launching as many campaigns as possible that we've forgotten to target our loyal customers",
    name: "Roy Smith",
    role: "Developer",
  },
  {
    image: "https://themewagon.github.io/pavo/images/testimonial-3.jpg",
    text: "I've been searching for a tool like Pavo for so long. I love the reports it generates and the amazing high accuracy",
    name: "Marsha Singer",
    role: "Marketer",
  },
];
</script>

<style scoped>
.app {
  display: flex;
  align-items: center;
  justify-content: space-between;
  padding: 4rem 4rem;
  background: skyblue;
}
.kkk {
  text-align: center;
  font-size: 30px;
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

/* Mobile Adjustments */
@media (max-width: 768px) {
  .app {
    flex-direction: column;
    text-align: center;
    padding: 2rem 1rem;
  }
  .kkk {
    text-align: left;
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

/* Features Page */
.features-section {
  padding: 4rem 0;
  text-align: center;
  background-color: #f5f8fa;
}

.features-heading {
  font-size: 3rem;
  font-weight: bold;
  margin-bottom: 2rem;
}

.features-container {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 2rem;
  max-width: 75rem;
  margin: 0 auto;
}

.feature-box {
  text-align: center;
  background: lightblue;
  padding: 1.5rem;
  border-radius: 10px;
  box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
  transition: transform 0.3s ease, box-shadow 0.3s ease;
}

.feature-box:hover {
  transform: translateY(-5px);
  box-shadow: 0 6px 10px rgba(0, 0, 0, 0.15);
}

.feature-box img {
  width: 64px;
  height: 64px;
  margin-bottom: 1rem;
  margin-left: 35%;
}

.feature-box h2 {
  font-size: 1.2rem;
  margin-bottom: 0.8rem;
}

.feature-box p {
  font-size: 0.9rem;
}

@media (max-width: 768px) {
  .features-container {
    grid-template-columns: 1fr 1fr;
  }

  .feature-box {
    padding: 1rem;
  }

  .features-heading {
    font-size: 2rem;
    margin-top: -2rem;
  }

  .feature-box img {
    margin: 0 auto 1rem auto;
  }
}

/*Details section*/

.detailsbutton {
  display: flex;
  flex-direction: row;
  gap: 2rem;
  margin-top: 2rem;
  margin-bottom: 2rem;
}

.statistics-container {
  display: flex;
  justify-content: center;
  gap: 5rem;
  margin-top: 1rem;
}

.stat-box h2 {
  font-weight: 500;
  font-size: 3rem;
}

.stat-box p {
  font-size: 1rem;
  color: #be1599;
}

#Details {
  display: flex;
  align-items: left;
  justify-content: space-between;
  width: 80%;
  gap: 6.25rem;
}

#Details .dataa {
  width: 70%;
}

#Details .details-images {
  width: 30rem;
}

#Details .data1 {
  display: flex;
  flex-direction: column;
  align-items: left;
  justify-content: center;
}

.data1 h1 {
  display: flex;
  font-size: 2rem;
  width: 60%;
}

.data1 .p {
  width: 80%;
  margin-top: 1.8rem;
}

.head2 {
  text-align: left;
  font-weight: bold;
  font-size: 3rem;
  margin-bottom: 1rem;
  color: rgb(8, 7, 7);
}

@media (max-width: 768px) {
  .statistics-container {
    flex-direction: column;
    gap: 2rem;
    padding: 0 1rem;
  }
  .detailsbutton {
    margin-left: 2rem;
  }
  .stat-box {
    display: flex;
    flex-direction: column;
    align-items: center;
    width: 100%;
    margin: 1rem 0;
  }
  .stat-box h2 {
    font-size: 2.5rem;
    text-align: left;
  }

  #Details {
    flex-direction: column;
    align-items: center;
    gap: 2rem;
    width: 90%;
    padding: 0;
  }

  #Details .dataa {
    width: 100%;
    text-align: left;
  }

  #Details .details-images {
    width: 100%;
    max-width: 31rem;
  }

  .data1 h1 {
    font-size: 1.5rem;
    width: 100%;
  }

  .data1 .p {
    width: 90%;
    margin-top: 1rem;
    font-size: 0.9rem;
  }

  .head2 {
    font-size: 2rem;
    margin-bottom: 1.5rem;
  }
  .detailsheading {
    font-size: 1.5rem;
    padding: 0%;
    width: 100%;
  }
  .heading1 {
    font-size: 1.5rem;
  }
}

/* Pricing Section */
#Pricing {
  background-image: url("https://www.shutterstock.com/image-photo/group-colleagues-engaging-discussion-during-600nw-2461746317.jpg");
  background-size: cover;
  background-position: center;
  background-repeat: no-repeat;
  position: relative;
  color: black;
  padding: 2rem 1rem;
}

#Pricing::before {
  content: "";
  position: absolute;
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;
  background: rgba(80, 80, 80, 0.5);
  z-index: 0;
}

#Pricing .pricing-container,
#Pricing .pricing-heading,
#Pricing .par {
  position: relative;
  z-index: 2;
}

.pricing-container {
  display: flex;
  justify-content: center;
  gap: 2rem;
  margin-top: 2rem;
  flex-wrap: wrap;
}

.pricing-heading {
  text-align: center;
  font-weight: bold;
  font-size: 3rem;
  margin-bottom: 1rem;
  color: black;
}

.par {
  text-align: center;
  color: rgb(66, 65, 65);
}

.pricing-box {
  background: rgba(255, 255, 255, 0.8);
  padding: 2rem;
  text-align: center;
  flex: 1;
  max-width: 18rem;
  border-radius: 10px;
  transition: transform 0.3s ease, box-shadow 0.3s ease;
}

.pricing-box:hover {
  transform: translateY(-5px);
  box-shadow: 0 6px 10px rgba(0, 0, 0, 0.15);
}

.pricing-box h2 {
  font-size: 1.5rem;
  margin-bottom: 1rem;
}

.price {
  font-size: 2rem;
  font-weight: bold;
  margin-bottom: 1rem;
}

.price span {
  font-size: 1rem;
}

@media (max-width: 768px) {
  .pricing-container {
    flex-direction: column;
    gap: 1rem;
  }

  .pricing-box {
    max-width: 100%;
  }

  .pricing-box h2 {
    font-size: 1.3rem;
  }

  .price {
    font-size: 1.6rem;
  }

  .pricing-heading {
    text-align: center;
    font-size: 2rem;
    padding: 1rem;
  }
}

/* Download Section */
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
  text-align: center;
  font-weight: bold;
  font-size: 1rem;
  margin-top: 2rem;
}
.download-buttons {
  margin-top: 2rem;
}

@media (max-width: 768px) {
  .download-container {
    flex-direction: column;
    width: 100%;
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

  .btn {
    padding: 1rem;
    font-size: 1rem;
  }

  .head5 {
    font-size: 0.9rem;
  }
  .public {
    font-size: 0.6rem;
  }
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
  gap: 0.5rem;
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
}
.container {
  max-width: 75rem;
  margin: 0 auto;
  padding: 0 1.5rem;
}
</style>
