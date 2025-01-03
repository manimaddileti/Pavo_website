<template>
  <div class="flex flex-col justify-between p-4 lg:p-20">
    <div class="grid grid-cols-1 lg:grid-cols-2 gap-10">
      <div class="flex flex-col justify-center items-center">
        <h2>Results driven ground breaking technology</h2>
        <p>
          Based on our team's extensive experience in developing line of
          business applications and constructive customer feedback we reached a
          new level of revenue.
        </p>

        <p>
          We enjoy helping small and medium sized tech businesses take a shot at
          established Fortune 500 companies
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
      <div class="flex flex-col justify-center items-center">
        <h2>Results driven ground breaking technology</h2>
        <ol class="order">
          <li>> Features that will help you and your marketers.</li>
          <li>> mooth learning curve due to the knowledge base.</li>
          <li>> Ready out-of-the-box with minor setup settings.</li>
          <div class="dbutton">
            <a href="" class="btn blue">Lightbox</a>
            <a href="" class="btn pink">Details</a>
          </div>
        </ol>
      </div>
    </div>

    <div class="grid grid-cols-1 lg:grid-cols-2 gap-10">
      <div class="flex flex-col justify-center items-center">
        <h2>Results driven ground breaking technology</h2>
        <p>
          Get a glimpse of what this app can do for your marketing automation
          and understand why current users are so excited when using Pavo
          together with their teams.
        </p>

        <p>
          We will promptly answer any questions and honor your requests based on
          the service level agreement
        </p>
      </div>

      <div class="details-images">
        <img :src="detailsImage3" />
      </div>
    </div>
  </div>
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
          <h3 class="font-bold text-gray-800 text-center">
            {{ users.name }} - {{ users.role }}
          </h3>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup lang="ts">
import { detailsImage1, detailsImage2, detailsImage3 } from "~/assets/img/images";
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
  gap: 3rem;
  margin-top: 1rem;
}

.stat-box h2 {
  font-weight: 600;
  font-size: 3.5rem;
}

.stat-box p {
  font-size: 1rem;
  color: lightblack;
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
  .details-images {
    margin-bottom: 2.5rem;
  }
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
.order {
  color: #6b747b;
  font: 400 1rem/1.625rem "Open Sans", sans-serif;
  margin-bottom: 1rem;
}
.btn.blue {
  background-color: skyblue;
  color: black;
  padding: 0.8rem 1.5rem;
  border-radius: 10px;
}
.btn.pink {
  padding: 0.8rem 1.5rem;
  border-radius: 10px;
  background-color: lightpink;
  color: black;
}
.dbutton {
  display: flex;
  flex-direction: row;
  gap: 1rem;
  margin-top: 1.3rem;
  cursor: pointer;
}
</style>
