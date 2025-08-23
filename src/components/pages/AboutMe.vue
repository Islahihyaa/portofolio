<script setup>
import { ref } from 'vue'
import ButtonLight from '../ui/ButtonLight.vue'
import Person from '../icons/Person.vue'
import Education from '../icons/Education.vue'
import Fire from '../icons/Fire.vue'
import Email from '../icons/Email.vue'
import Phone from '../icons/Phone.vue'
import Linkedin from '../icons/Linkedin.vue'
import Github from '../icons/Github.vue'
import Instagram from '../icons/Instagram.vue'

const aboutMe = ref({
  summary: `
    <div class="space-y-4 leading-relaxed text-gray-700">

      <p>
        I’m a <span class="font-semibold text-indigo-600">detail-oriented individual</span> 
        with a solid foundation in the 
        <span class="font-semibold text-indigo-600">full software development lifecycle</span>, 
        from <span class="font-semibold">requirements gathering</span> and 
        <span class="font-semibold">system design</span> 
        to <span class="font-semibold">testing and deployment</span>. 
        Experienced in <span class="font-semibold">analyzing business processes</span>, 
        <span class="font-semibold">translating stakeholder needs into functional and technical specifications</span>, 
        and creating clear documentation such as 
        <span class="font-semibold">use cases, ERD, and system flow diagrams</span>.
      </p>

      <p>
        My background in <span class="font-semibold text-indigo-600">frontend and backend development</span> 
        using <span class="font-semibold">JavaScript, PHP, Python, TypeScript, and Java</span> 
        allows me to effectively 
        <span class="font-semibold text-indigo-600">bridge the gap between business requirements and technical implementation</span>. 
        I am familiar with <span class="font-semibold">secure and scalable system design</span>, including 
        <span class="font-semibold">authentication mechanisms, real-time communication, and message queuing</span>.
      </p>

      <p>
        Skilled in collaborating within <span class="font-semibold text-indigo-600">agile teams</span> 
        using tools like <span class="font-semibold">GitLab, GitHub, ClickUp, Jira, and Slack</span>, 
        I bring <span class="font-semibold text-indigo-600">analytical thinking, communication, and problem-solving abilities</span> 
        to deliver <span class="font-semibold text-green-600">effective and reliable system solutions</span>.
      </p>

    </div>
  `,
})

const contacts = ref([
  {
    label: 'LinkedIn',
    icon: Linkedin,
    href: 'https://www.linkedin.com/in/islahihyamuhammad/',
  },
  {
    label: 'GitHub',
    icon: Github,
    href: 'https://github.com/Islahihyaa',
  },
  {
    label: 'Instagram',
    icon: Instagram,
    href: 'https://www.instagram.com/islahihyaa/',
  },
])
</script>

<template>
  <section
    class="max-w-screen-2xl mx-2 sm:mx-auto px-4 sm:px-6 lg:px-0 py-6 pb-20 sm:py-8 rounded-[2.25rem] sm:rounded-xl bg-white shadow-lg sm:shadow-md transform lg:-translate-y-12"
  >
    <div class="rotate-in w-full flex flex-col px-10">
      <div class="flex items-center mb-6 gap-4 text-blue-500 rotate-in-heading">
        <Person />
        <h1 class="font-bold text-xl">About me</h1>
      </div>
      <div class="rotate-in-pargh" v-html="aboutMe.summary"></div>

      <div class="flex items-center mt-4 mb-6 gap-4 text-blue-500 rotate-in-heading">
        <Education />
        <h1 class="font-bold text-xl">Education</h1>
      </div>
      <div class="rotate-in-pargh">
        <h2><b>Telkom University</b></h2>
        <p>Bachelor of Information Systems</p>
        <p>GPA : 3.79</p>
      </div>

      <div class="flex items-center mt-4 mb-6 gap-4 text-blue-500 rotate-in-heading">
        <Fire />
        <h1 class="font-bold text-xl">Interest</h1>
      </div>
      <div class="rotate-in-pargh flex flex-wrap gap-4">
        <p class="bg-blue-100 p-2 rounded-md font-semibold">Full stack Development</p>
        <p class="bg-blue-100 p-2 rounded-md font-semibold">IT System Analyst</p>
        <p class="bg-blue-100 p-2 rounded-md font-semibold">Front End Development</p>
        <p class="bg-blue-100 p-2 rounded-md font-semibold">Back End Development</p>
        <p class="bg-blue-100 p-2 rounded-md font-semibold">Software Engineering</p>
        <p class="bg-blue-100 p-2 rounded-md font-semibold">Mobile Development</p>
      </div>

      <h1 class="font-semibold text-xl text-blue-500 mt-4 mb-2 rotate-in-heading">
        You Can Find Me Here
      </h1>
      <div class="flex space-x-2 rotate-in-pargh">
        <a
          v-for="(contact, index) in contacts"
          :key="index"
          :href="contact.href"
          target="_blank"
          rel="noopener noreferrer"
        >
          <ButtonLight>
            <component :is="contact.icon" class="w-5 h-5" />
          </ButtonLight>
        </a>
      </div>
    </div>
  </section>
</template>

<style scoped>
@keyframes rotateIn {
  from {
    opacity: 0;
    transform: rotate(-10deg) translateY(20px);
  }
  to {
    opacity: 1;
    transform: rotate(0deg) translateY(0);
  }
}

.rotate-in {
  animation: rotateIn 0.8s ease-out forwards;
  opacity: 0;
}

.rotate-in-heading {
  animation: rotateIn 1.2s ease-out forwards;
  opacity: 0;
}

.rotate-in-pargh {
  animation: rotateIn 1.4s ease-out forwards;
  opacity: 0;
}
</style>
