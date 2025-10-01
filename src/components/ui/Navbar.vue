<script setup>
import { ref, onMounted, onUnmounted } from 'vue'
import NavPopup from '../ui/NavPopup.vue'
import Hamburger from '../icons/HamburgerIcon.vue'

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

onUnmounted(() => {
  window.removeEventListener('scroll', handleScroll)
})
</script>

<template>
  <!-- Navbar Mobile -->
  <div
    class="fixed top-4 right-6 md:hidden z-50 transition-all duration-300"
    :class="
      isScrolled
        ? 'top-1 w-full bg-white/80 backdrop-blur shadow-md rounded-none px-4 py-0'
        : 'right-0'
    "
  >
    <div
      :class="
        isScrolled
          ? 'flex justify-end items-center'
          : 'bg-white/80 backdrop-blur shadow-md rounded-full'
      "
    >
      <button @click="toggleNavbar" class="flex justify-end p-2">
        <Hamburger />
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
</template>
