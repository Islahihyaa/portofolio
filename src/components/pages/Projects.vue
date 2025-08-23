<script setup>
import { ref } from 'vue'
import quizMain from '@/assets/images/mockup/quiz-main.png'
import ObeMain from '@/assets/images/mockup/obe-mockup.png'
import TrelloMain from '@/assets/images/mockup/trello-mockup.png'
import FoodMain from '@/assets/images/mockup/food-mockup.png'
import WhizMain from '@/assets/images/mockup/whiz-mockup.png'
import ContactMain from '@/assets/images/mockup/contact-mockup.png'
import SAMain from '@/assets/images/mockup/systemAnalyst-mockup.png'
import quizExtra1 from '@/assets/images/mockup/desain/login.jpg'
import quizExtra2 from '@/assets/images/mockup/desain/regs.jpg'
import TrelloExtra1 from '@/assets/images/mockup/desain/trello-create.jpg'
import TrelloExtra2 from '@/assets/images/mockup/desain/trello-list.jpg'
import TrelloExtra3 from '@/assets/images/mockup/desain/trello-task.jpg'
import TrelloExtra4 from '@/assets/images/mockup/desain/trello-share.jpg'
import TrelloExtra5 from '@/assets/images/mockup/desain/trello-realtime.jpg'
import TrelloExtra6 from '@/assets/images/mockup/desain/trello-dragndrop.jpg'
import FoodExtra1 from '@/assets/images/mockup/desain/food-admin.jpg'
import FoodExtra2 from '@/assets/images/mockup/desain/food-adminlist.jpg'
import FoodExtra3 from '@/assets/images/mockup/desain/food-adminorder.jpg'
import FoodExtra4 from '@/assets/images/mockup/desain/food-home.jpg'
import FoodExtra5 from '@/assets/images/mockup/desain/food-homeadd.jpg'
import FoodExtra6 from '@/assets/images/mockup/desain/food-order.jpg'
import FoodExtra7 from '@/assets/images/mockup/desain/food-delv.jpg'
import FoodExtra8 from '@/assets/images/mockup/desain/food-payment.jpg'
import WhizExtra1 from '@/assets/images/mockup/desain/whiz-login.jpg'
import WhizExtra2 from '@/assets/images/mockup/desain/whiz-homejpg.jpg'
import WhizExtra3 from '@/assets/images/mockup/desain/whiz-biodata.jpg'
import ObeExtra1 from '@/assets/images/mockup/desain/obe-upload.jpg'
import ObeExtra2 from '@/assets/images/mockup/desain/obe-monitoring.jpg'
import SADocs from '@/assets/images/mockup/desain/SystemAnalyst_Islahihya Muhammad Jel Shibyan_1202210236.pdf'
import githubLogo from '@/assets/images/github-logo.png'
import Vue from '@/assets/logo.svg'
import React from '@/assets/images/logo/1.png'
import ExpressJS from '@/assets/images/logo/4.png'
import MySQL from '@/assets/images/logo/14.png'
import Laravel from '@/assets/images/logo/15.png'
import RabbitMQ from '@/assets/images/logo/12.png'
import MongoDB from '@/assets/images/logo/13.png'

const showPopup = ref(false)
const selectedProject = ref(null)
const currentMediaIndex = ref(0)

const projects = [
  {
    id: 1,
    title: 'Quizz Web Application',
    description:
      'An engaging and fully interactive Quiz Web Appdesigned to deliver a seamless and modern learning experience. ',
    details: `
    <p> <b> [ Demo Available ] </b> </p>
    <p>
      An engaging and fully interactive <b>Quiz Web App</b> designed to deliver a seamless and modern learning experience. 
      This application empowers users to <b>take quizzes, create their own, track progress,</b> and resume unfinished quizzes anytime—even after closing the browser.
    </p>

    <p class="mt-2"><b>✨ Key Highlights:</b></p>

    <ul class="list-disc ml-5 mt-2 space-y-0">
      <li><b>🔐 Secure Authentication</b> – Complete login & registration system to personalize every user’s journey.</li>
      <li><b>📝 Create Your Own Quiz</b> – A flexible quiz builder that allows users to design quizzes however they want.</li>
      <li><b>⏱️ Smart Question Timer</b> – Each question comes with its own timer to add challenge and excitement.</li>
      <li><b>💾 Auto-Save & Resume Progress</b> – Never lose track; continue your quiz exactly where you left off.</li>
      <li><b>📊 Comprehensive Results Dashboard</b> – Get instant scoring, performance summary, and insights at the end of every quiz.</li>
      <li><b>📱 Fully Responsive</b> – Optimized for all devices, ensuring a smooth experience on desktop, tablet, and mobile.</li>
    </ul>

    <p class="mt-1">
      With a scalable architecture and polished design, this project reflects my ability to build real-world applications that combine <b>functionality, user experience,</b> and <b>performance optimization</b>. 
      It’s not just a quiz app—it’s a <b>complete digital learning platform</b> crafted to demonstrate innovation, precision, and technical expertise.
    </p>
  `,
    media: [
      { type: 'image', src: quizMain },
      { type: 'image', src: quizExtra1 },
      { type: 'image', src: quizExtra2 },
      { type: 'video', src: 'https://youtu.be/OW4aiv4iCUQ' },
    ],
    techStack: [
      { name: 'React', logo: React },
      { name: 'Express JS', logo: ExpressJS },
      { name: 'MySQL', logo: MySQL },
    ],
    github: githubLogo,
    githubLink: 'https://github.com/Islahihyaa/quizkuy-app',
  },
  {
    id: 2,
    title: 'Outcome-Based Education Web Dashboard',
    description:
      'A powerful and intelligent web platform built to streamline academic performance tracking and evaluation in higher education',
    details: `
    <p> <b> [ Demo Available ] </b> </p>
    <p>
      A powerful and intelligent <b>web platform</b> built to streamline <b>academic performance tracking</b> and evaluation in higher education. This dashboard empowers educators and institutions to seamlessly manage student learning outcomes, ensuring <b>transparency, efficiency,</b> and <b>scalability</b>.
    </p>

    <p class="mt-2"><b>✨ Key Features:</b></p>

    <ul class="list-disc ml-5 mt-2 space-y-1">
      <li><b>🔐 Secure Authentication</b> – Robust login and role-based access (Admin, Lecturer, Student) for data security and personalized experience.</li>
      <li><b>📂 Fast & Large-Scale File Upload</b> – Supports Excel/CSV data uploads up to 500MB with optimized chunked upload and real-time progress tracking.</li>
      <li><b>📊 Automated Student Performance Calculation</b> – Instantly processes raw student scores into CLO (Course Learning Outcome) and PLO (Program Learning Outcome) achievements.</li>
      <li><b>📈 Interactive Analytics & Reports</b> – Visualize student performance trends with charts, graphs, and insights for curriculum improvement.</li>
      <li><b>🧩 Curriculum Mapping</b> – Connects each question/assessment to specific CLOs and PLOs for measurable outcomes.</li>
      <li><b>🛠️ Scalable Architecture</b> – Designed to handle large datasets and multi-user access without compromising performance.</li>
      <li><b>📱 Responsive & Modern UI</b> – Accessible across devices with a sleek, intuitive interface tailored for both educators and administrators.</li>
      <li><b>⏳ Data Resume & Auto-Save</b> – Ensures uninterrupted data processing even if the browser or session is closed unexpectedly.</li>
    </ul>

    <p class="mt-3">
      🚀 This project showcases my ability to <b>design and develop a real-world EdTech solution</b> that bridges technology with education. The <b>OBE Dashboard</b> not only simplifies data management but also transforms complex assessment systems into <b>actionable insights</b> for continuous academic improvement.
    </p>
  `,
    media: [
      { type: 'image', src: ObeMain },
      { type: 'image', src: ObeExtra1 },
      { type: 'image', src: ObeExtra2 },
      { type: 'video', src: 'https://youtu.be/-6XhjNbZn5s' },
    ],
    techStack: [
      { name: 'Laravel', logo: Laravel },
      { name: 'MySQL', logo: MySQL },
    ],
    github: githubLogo,
    githubLink: 'https://github.com/orgs/Telyu-SI/teams/obe-team/repositories',
  },
  {
    id: 3,
    title: 'Trello Management Task Web App',
    description:
      'A modern, collaborative task management platformdesigned to boost productivity and streamline project workflows',
    details: `
    <p>
      A modern, collaborative <b>task management platform</b> designed to boost productivity and streamline project workflows. Inspired by Trello, this application combines <b>real-time collaboration</b> with an <b>intuitive, responsive interface</b> to help teams organize, prioritize, and complete tasks efficiently.
    </p>

    <p class="mt-2"><b>✨ Key Features:</b></p>

    <ul class="list-disc ml-5 mt-2 space-y-1">
      <li><b>🖥️ Responsive & User-Friendly Interface</b> – Built with a sleek design that adapts seamlessly across desktop and mobile.</li>
      <li><b>📝 Flexible Task Management</b> – Users can create, edit, and organize tasks into customizable lists for better project structure.</li>
      <li><b>📋 Board & List System</b> – Mimics Trello’s functionality, allowing clear visualization of project stages and progress.</li>
      <li><b>👥 Board Sharing & Collaboration</b> – Share boards with teammates or external accounts for collaborative project management.</li>
      <li><b>🔄 Real-Time Updates</b> – Every change is synchronized instantly, ensuring all team members see the most up-to-date information.</li>
      <li><b>📡 Scalable Collaboration</b> – Supports multiple users working simultaneously without data conflicts.</li>
      <li><b>🔐 Secure Access Control</b> – Ensure only authorized users can view or modify shared boards.</li>
      <li><b>🚀 Optimized Performance</b> – Designed for fast, smooth interactions even with multiple concurrent users.</li>
    </ul>

    <p class="mt-3">
      This project demonstrates my ability to <b>build real-time web applications</b>, integrating <b>state management, live updates, and collaborative features</b>. 
      It’s more than a simple task tracker—it’s a <b>powerful teamwork platform</b> that highlights my skills in modern web development and scalable system design.
    </p>
  `,
    media: [
      { type: 'image', src: TrelloMain },
      { type: 'image', src: TrelloExtra1 },
      { type: 'image', src: TrelloExtra2 },
      { type: 'image', src: TrelloExtra3 },
      { type: 'image', src: TrelloExtra4 },
      { type: 'image', src: TrelloExtra5 },
      { type: 'image', src: TrelloExtra6 },
    ],
    techStack: [
      { name: 'Vue', logo: Vue },
      { name: 'ExpressJS', logo: ExpressJS },
      { name: 'MySQL', logo: MySQL },
    ],
    github: githubLogo,
    githubLink: 'https://github.com/Islahihyaa/intern-btsid-fe-ihya',
  },
  {
    id: 4,
    title: 'Food Delivery UMKM',
    description:
      'Food delivery application for UMKM with real-time order features and product management.',
    details: `
    <p>
      A comprehensive <b>food delivery web application</b> built to support local small businesses (UMKM) by providing a <b>seamless digital ordering experience</b>. Designed with a <b>dynamic and responsive UI</b>, the platform ensures both customers and administrators can interact efficiently in real-time.
    </p>

    <p class="mt-2"><b>✨ Key Features:</b></p>

    <ul class="list-disc ml-5 mt-2 space-y-1">
      <li><b>🖥️ Dynamic & Responsive Interface</b> – Optimized for smooth experience across desktop and mobile devices.</li>
      <li><b>👥 Role-Based Access</b> – Separate dashboards for Admins and Customers with tailored features.</li>
      <li><b>🍽️ Customer Experience</b> – Browse menus, select food items, place orders, and complete payments with ease.</li>
      <li><b>🛠️ Admin Management</b> – Admins can manage products, update menus, and track incoming customer orders.</li>
      <li><b>📡 Event-Driven Architecture</b> – Implemented pub/sub communication with RabbitMQ to enable fast, reliable, and scalable interactions between services.</li>
      <li><b>🔄 Real-Time Order Updates</b> – Customers receive live status updates on their orders (e.g., pending, confirmed, delivered).</li>
      <li><b>💳 Integrated Payment System</b> – Supports secure online payments for hassle-free transactions.</li>
      <li><b>🚀 Scalable & Maintainable</b> – Designed with microservice principles for future growth and integration.</li>
    </ul>

    <p class="mt-1">
      This project showcases my expertise in <b>building full-stack applications</b> with <b>event-driven microservice architecture</b>, blending <b>user experience, scalability, and real-time data flow</b>. More than just a food delivery app, it’s a <b>digital ecosystem</b> to empower local businesses and connect them with customers seamlessly.
    </p>
  `,
    media: [
      { type: 'image', src: FoodMain },
      { type: 'image', src: FoodExtra1 },
      { type: 'image', src: FoodExtra2 },
      { type: 'image', src: FoodExtra3 },
      { type: 'image', src: FoodExtra4 },
      { type: 'image', src: FoodExtra5 },
      { type: 'image', src: FoodExtra6 },
      { type: 'image', src: FoodExtra7 },
      { type: 'image', src: FoodExtra8 },
    ],
    techStack: [
      { name: 'React', logo: React },
      { name: 'ExpressJS', logo: ExpressJS },
      { name: 'MongoDB', logo: MongoDB },
      { name: 'RabbitMQ', logo: RabbitMQ },
    ],
    github: githubLogo,
    githubLink: 'https://github.com/Islahihyaa/UMKM-Delivery-Food',
  },
  {
    id: 5,
    title: 'WhizCycle Dashboard',
    description:
      'An interactive platform to manage and provide incentives for recycling activities.',
    details: `
    <p>
      A <b>smart and interactive web platform</b> designed to manage and incentivize recycling activities. <b>WhizCycle empowers communities</b> to actively participate in waste recycling through a <b>seamless digital experience</b> that combines scheduling, tracking, and reward systems.
    </p>

    <p class="mt-2"><b>✨ Key Features:</b></p>

    <ul class="list-disc ml-5 mt-2 space-y-1 leading-snug">
      <li><b>♻️ Recycling Management</b> – Users can schedule and manage waste collection with ease.</li>
      <li><b>🗓️ Waste Pickup Scheduling</b> – Set and track pickup times for different types of waste.</li>
      <li><b>🎁 Point Reward System</b> – Earn points for every recycling contribution.</li>
      <li><b>📜 Contribution History</b> – View a complete record of past recycling activities.</li>
      <li><b>🔄 Point Redemption</b> – Exchange accumulated points for rewards or benefits.</li>
      <li><b>📱 User-Friendly Dashboard</b> – Clean, responsive, and intuitive design accessible across devices.</li>
      <li><b>🚀 Community Empowerment</b> – Encourages eco-friendly habits by making recycling rewarding and trackable.</li>
    </ul>

    <p class="mt-3">
      This project highlights my ability to <b>design and develop sustainable tech solutions</b> that merge <b>functionality, user engagement, and social impact</b>. WhizCycle Dashboard is more than just a platform—it’s a <b>step toward a smarter, greener, and more responsible future</b>. 🌍
    </p>
  `,
    media: [
      { type: 'image', src: WhizMain },
      { type: 'image', src: WhizExtra1 },
      { type: 'image', src: WhizExtra2 },
      { type: 'image', src: WhizExtra3 },
    ],
    techStack: [
      { name: 'Laravel', logo: Laravel },
      { name: 'MySQL', logo: MySQL },
    ],
    github: githubLogo,
    githubLink: 'https://github.com/Islahihyaa/dashboard-WhizCycle-RPL/tree/islahihya',
  },
  {
    id: 6,
    title: 'Get Contact Backend',
    description:
      'A backend service built with Node JS, Prisma, and RabbitMQ to handle contact management in a fast, scalable, and event-driven way.',
    details: `
    <p>
      A <b>backend service</b> built with <b>Node.js, Prisma, and RabbitMQ</b> to handle <b>contact management</b> in a <b>fast</b>, <b>scalable</b>, and <b>event-driven</b> way. Contact data is stored securely in the database while also being <b>published to a message queue</b> for real-time processing by other services.
    </p>

    <p class="mt-2"><b>✨ Key Features:</b></p>

    <ul class="list-disc ml-5 mt-2 space-y-1 leading-snug">
      <li><b>🗄️ Contact Management</b> – Validate and store contact data using Prisma ORM.</li>
      <li><b>📡 Event-Driven Messaging</b> – Publish contact data to RabbitMQ for asynchronous processing.</li>
      <li><b>🔄 Reliable Communication</b> – Uses durable queues and exchanges to ensure data consistency.</li>
      <li><b>🚀 Scalable Architecture</b> – Decoupled design allows easy integration with other microservices.</li>
    </ul>

    <p class="mt-3">
      This project demonstrates my ability to build <b>modern, event-driven backends</b> that combine <b>database reliability</b> with <b>real-time messaging</b> for <b>scalable applications</b>.
    </p>
  `,
    media: [
      { type: 'image', src: ContactMain },
      { type: 'image', src: ContactMain },
      { type: 'image', src: ContactMain },
    ],
    techStack: [
      { name: 'ExpressJS', logo: ExpressJS },
      { name: 'MongoDB', logo: MongoDB },
      { name: 'RabbitMQ', logo: RabbitMQ },
    ],
    github: githubLogo,
    githubLink: 'https://github.com/Islahihyaa/get_contact_with_restfulapi_rabbitmq',
  },
  {
    id: 7,
    title: 'SRS (Software Requirement Specification Documentation',
    description:
      'Comprehensive documentation containing end-to-end system analysis, requirements, workflows, and design specifications.',
    details: `
    <p>
      A <b>comprehensive document</b> that contains the <b>end-to-end analysis of a system</b>, detailing <b>requirements, workflows, and design specifications</b>. This documentation serves as a <b>blueprint</b> for developers, stakeholders, and project managers to ensure the system is built according to business needs and technical feasibility.
    </p>

    <p class="mt-2"><b>✨ Key Contents:</b></p>

    <ul class="list-disc ml-5 mt-2 space-y-1 leading-snug">
      <li><b>📌 Business Requirement Analysis</b> – Identifying stakeholder needs and translating them into clear system goals.</li>
      <li><b>🔄 System Workflow & Use Case Diagrams</b> – Visual representation of processes, user interactions, and data flows.</li>
      <li><b>🗂️ Data Modeling</b> – ERD (Entity Relationship Diagram) and database structure design for efficient data management.</li>
      <li><b>⚙️ Functional & Non-Functional Requirements</b> – Detailed breakdown of features, performance, and system constraints.</li>
      <li><b>🏗️ System Architecture Design</b> – High-level and detailed design of the system components and integrations.</li>
      <li><b>🧩 Gap Analysis & Feasibility Study</b> – Comparing current systems with proposed solutions to identify improvements.</li>
      <li><b>📊 Supporting Documentation</b> – Mockups, prototypes, and technical notes for development references.</li>
    </ul>

    <p class="mt-3">
      This document reflects my ability as a <b>System Analyst</b> to <b>bridge communication between business and technical teams</b>, ensuring that the system developed is <b>aligned with organizational objectives</b>, <b>scalable</b>, and <b>user-centered</b>.
    </p>
  `,
    media: [
      { type: 'image', src: SAMain },
      { type: 'document', src: SADocs },
    ],
    github: githubLogo,
    githubLink:
      'https://drive.google.com/file/d/1TlNZNW-Gf8gtywEGf9idoWQwUniNpgjS/view?usp=sharing',
  },
]

const toEmbedUrl = (url) => {
  if (url.includes('youtu.be')) {
    const id = url.split('youtu.be/')[1]
    return `https://www.youtube.com/embed/${id}`
  }
  if (url.includes('watch?v=')) {
    const id = url.split('watch?v=')[1]
    return `https://www.youtube.com/embed/${id}`
  }
  return url
}

const openPopup = (project) => {
  selectedProject.value = project
  showPopup.value = true
}

const closePopup = () => {
  showPopup.value = false
  selectedProject.value = null
}

const nextMedia = () => {
  if (!selectedProject.value) return
  currentMediaIndex.value = (currentMediaIndex.value + 1) % selectedProject.value.media.length
}

const prevMedia = () => {
  if (!selectedProject.value) return
  currentMediaIndex.value =
    (currentMediaIndex.value - 1 + selectedProject.value.media.length) %
    selectedProject.value.media.length
}
</script>

<template>
  <div class="flex flex-col items-center justify-center">
    <h1 class="font-bold text-4xl text-blue-500 mb-10">Projects</h1>
    <div class="container-project">
      <div class="flex flex-wrap justify-center gap-6">
        <!-- Loop semua projects -->
        <div
          v-for="project in projects"
          :key="project.id"
          @click="openPopup(project)"
          class="flex flex-col gap-4 w-[400px] bg-gray-50 p-4 rounded-xl hover:shadow-xl transition-all cursor-pointer"
        >
          <div
            v-if="project.media && project.media.find((m) => m.type === 'image')"
            class="flex justify-center items-center bg-gray-200 rounded-xl overflow-hidden hover:shadow-md transition-all w-full h-80"
          >
            <img
              :src="project.media.find((m) => m.type === 'image').src"
              alt="project"
              class="w-full h-full object-contain"
            />
          </div>
          <div class="px-3">
            <div class="flex justify-between">
              <h3 class="text-start text-md font-medium text-gray-900 mt-2">{{ project.title }}</h3>
              <div class="flex justify-center items-center gap-4">
                <a :href="project.githubLink" target="_blank" rel="noopener noreferrer" @click.stop>
                  <div
                    class="bg-blue-300 rounded-full px-1.5 py-1.5 flex justify-center items-center"
                  >
                    <img :src="project.github" alt="" width="20" />
                  </div>
                </a>
              </div>
            </div>
            <p class="mt-3 text-gray-600 line-clamp-3">
              {{ project.description }}
            </p>

            <!-- Tech Stack -->
            <div class="flex flex-wrap items-center gap-2 mt-4">
              <img
                v-for="(tech, idx) in project.techStack"
                :key="idx"
                :src="tech.logo"
                :alt="tech.name"
                class="w-7 h-7 object-contain hover:scale-110 transition-transform"
                :title="tech.name"
              />
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>

  <!-- Popup -->
  <div
    v-if="showPopup && selectedProject"
    class="fixed inset-0 bg-black/50 backdrop-blur-sm flex justify-center items-center z-50"
  >
    <div
      class="bg-white w-[100%] md:w-[80%] lg:w-[70%] lg:h-[90%] p-8 rounded-2xl shadow-2xl relative"
    >
      <button
        class="absolute top-4 right-4 bg-gray-200 hover:bg-gray-300 rounded-full p-2"
        @click="closePopup"
      >
        ✕
      </button>

      <h2 class="text-2xl font-bold mb-4">{{ selectedProject.title }}</h2>

      <!-- Carousel -->
      <div
        class="relative w-full h-96 flex justify-center items-center bg-gray-200 rounded-lg overflow-hidden"
      >
        <template v-if="selectedProject.media[currentMediaIndex].type === 'image'">
          <img
            :src="selectedProject.media[currentMediaIndex].src"
            alt="media"
            class="w-full h-full object-contain"
          />
        </template>
        <template v-else-if="selectedProject.media[currentMediaIndex].type === 'video'">
          <iframe
            :src="toEmbedUrl(selectedProject.media[currentMediaIndex].src)"
            frameborder="0"
            allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture"
            allowfullscreen
            class="w-full h-full"
          />
        </template>
        <template v-else-if="selectedProject.media[currentMediaIndex].type === 'document'">
          <iframe
            :src="selectedProject.media[currentMediaIndex].src"
            class="w-full h-full"
          ></iframe>
        </template>

        <!-- Panah navigasi -->
        <button
          class="absolute left-2 bg-white/70 hover:bg-white p-2 rounded-full"
          @click.stop="prevMedia"
        >
          ◀
        </button>
        <button
          class="absolute right-2 bg-white/70 hover:bg-white p-2 rounded-full"
          @click.stop="nextMedia"
        >
          ▶
        </button>
      </div>

      <!-- Deskripsi -->
      <div
        class="text-gray-600 leading-snug mt-4 whitespace-pre-line overflow-y-auto max-h-80 pr-2 text-md"
        v-html="selectedProject.details"
      ></div>
    </div>
  </div>
</template>

<style setup>
.container-project {
  width: 70%;
}
</style>
