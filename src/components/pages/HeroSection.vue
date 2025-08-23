<script setup>
import { ref, onMounted, onUnmounted } from 'vue'
import Button from '../ui/Button.vue'
import Pattern from '../icons/Pattern.vue'
import Navbar from '../base/Navbar.vue'
import NavPopup from '../ui/NavPopup.vue'

const biodata = ref({
  name: 'Islahihya Muhammad Jel Shibyan',
  interest: [
    'Full Stack Web Development',
    'Front End Development',
    'Back End Development',
    'IT System Analyst',
    'DevSecOps',
  ],
  summary:
    'Professional with 2 years of experience in Information Technology, skilled in end-to-end software development, system analysis, and delivering scalable, secure, and user-friendly applications that effectively bridge business needs with technical implementation.',
})

const showNavbar = ref(false)
const isScrolled = ref(false)

const activeSection = ref('home')
const sections = ['about', 'skills', 'projects', 'experiences', 'testimonials', 'contacts']

const toggleNavbar = () => {
  showNavbar.value = !showNavbar.value
}

const handleScroll = () => {
  isScrolled.value = window.scrollY > 0
}

onMounted(() => {
  window.addEventListener('scroll', handleScroll)
})

onUnmounted(() => {
  window.removeEventListener('scroll', handleScroll)
})

onMounted(() => {
  const observer = new IntersectionObserver(
    (entries) => {
      entries.forEach((entry) => {
        if (entry.isIntersecting) {
          activeSection.value = entry.target.id
        }
      })
    },
    { threshold: 0.6 },
  )

  sections.forEach((id) => {
    const el = document.getElementById(id)
    if (el) observer.observe(el)
  })
})

onUnmounted(() => {})
</script>

<template>
  <section>
    <div
      class="fixed top-4 right-6 md:hidden z-50 transition-all duration-300"
      :class="
        isScrolled
          ? 'top-1 w-full bg-white/80 backdrop-blur shadow-md rounded-none right-0 px-4 py-0'
          : 'right-6'
      "
    >
      <div
        :class="
          isScrolled
            ? 'flex justify-end items-center'
            : 'bg-white/80 backdrop-blur shadow-md rounded-full'
        "
      >
        <button @click="toggleNavbar">
          <Navbar />
        </button>
      </div>

      <!-- Popup -->
      <NavPopup :show="showNavbar" @close="toggleNavbar" />
    </div>

    <!-- Navbar Dekstop -->
    <div
      class="fixed top-4 left-1/2 -translate-x-1/2 z-40 hidden md:block transition-all duration-300"
    >
      <div
        class="inline-flex items-center gap-6 bg-white/40 backdrop-blur-md rounded-full shadow-xl px-24 py-4"
      >
        <ul class="flex items-center gap-6 font-semibold text-lg">
          <li>
            <a
              href="#"
              :class="
                activeSection === 'about'
                  ? 'bg-blue-500 text-white px-4 py-2 rounded-full transition '
                  : 'text-blue-500 hover:bg-blue-500 hover:text-white px-4 py-2 rounded-full transition font-semibold'
              "
              >Home</a
            >
          </li>
          <li>
            <a
              href="#skills"
              :class="
                activeSection === 'skills'
                  ? 'bg-blue-500 text-white px-4 py-2 rounded-full transition '
                  : 'text-blue-500 hover:bg-blue-500 hover:text-white px-4 py-2 rounded-full transition font-semibold'
              "
              >Skills</a
            >
          </li>
          <li>
            <a
              href="#projects"
              :class="
                activeSection === 'projects'
                  ? 'bg-blue-500 text-white px-4 py-2 rounded-full transition '
                  : 'text-blue-500 hover:bg-blue-500 hover:text-white px-4 py-2 rounded-full transition font-semibold'
              "
              >Projects</a
            >
          </li>
          <li>
            <a
              href="#experiences"
              :class="
                activeSection === 'experiences'
                  ? 'bg-blue-500 text-white px-4 py-2 rounded-full transition '
                  : 'text-blue-500 hover:bg-blue-500 hover:text-white px-4 py-2 rounded-full transition font-semibold'
              "
              >Experiences</a
            >
          </li>
        </ul>
      </div>
    </div>

    <div
      class="flex flex-col md:flex-row items-center text-center md:text-left space-y-6 md:space-y-20 md:space-x-8"
    >
      <div class="md:w-2/5 flex justify-center mt-14">
        <img
          src="@/assets/images/my-foto-bg.png"
          alt="hero"
          class="rounded-xl border-b-4 border-t-4 border-blue-400"
          width="400"
        />
      </div>
      <div class="md:w-3/5 flex flex-col justify-center">
        <h3 class="text-2xl font-bold text-blue-400 mb-4">Hello, I'm</h3>
        <h1 class="text-6xl font-bold leading-tight">
          <em class="text-header-gradient">Islahihya</em> Muhammad <br />Jel
          <em class="text-header-gradient">Shibyan</em>
        </h1>
        <h2 class="text-xl font-bold my-4">{{ biodata.interest.join(' | ') }}</h2>
        <p class="py-4 font-semibold">{{ biodata.summary }}</p>
        <div class="space-x-4">
          <a href="https://wa.me/+6288215419786" target="_blank" rel="noopener noreferrer">
            <Button>Connect Now</Button>
          </a>
        </div>
      </div>
    </div>

    <Pattern />
  </section>
</template>

<style scoped>
.text-header-gradient {
  background: rgb(45, 126, 248);
  background: linear-gradient(
    169.4deg,
    #3984f4 -6.01%,
    #0cd3ff 36.87%,
    #2f7cf0 78.04%,
    #0e65e8 103.77%
  );
  background-clip: text;
  -webkit-text-fill-color: transparent;
  font:
    bold 60px/40px 'Open Sans',
    sans-serif;
}
</style>
