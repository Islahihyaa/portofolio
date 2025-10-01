<script setup>
import Navbar from '../ui/Navbar.vue'
import HeroSection from '../pages/HeroSection.vue'
import AboutMe from '../pages/AboutMe.vue'
import MySkills from '../pages/MySkills.vue'
import Projects from '../pages/Projects.vue'
import WorkExperience from '../pages/WorkExperience.vue'
import Comment from '../pages/Comment.vue'
import Contact from '../pages/Contact.vue'
</script>

<template>
  <div class="relative mx-auto">
    <Navbar/>
    <div class="cover-gradient pt-16 pb-32 px-4 ">
      <HeroSection />
    </div>
    <div id="about">
      <AboutMe />
    </div>
    <div id="skills" class="mt-12 mb-16 pt-16 pb-32 cover-gradient">
      <MySkills />
    </div>
    <div id="projects" class="mb-16">
      <Projects />
    </div>
    <div id="experiences" class="mb-24">
      <WorkExperience />
    </div>
    <!-- <div id="testimonials" class="mb-96">
      <Comment />
    </div>
    <div id="testimonials">
      <Contact />
    </div> -->
  </div>
</template>

<style scoped>
.cover-gradient {
  background: linear-gradient(
    169.4deg,
    rgba(6, 50, 116, 0.04) -6.01%,
    rgba(12, 211, 255, 0.04) 36.87%,
    rgba(47, 124, 240, 0.04) 78.04%,
    rgba(14, 101, 232, 0.04) 103.77%
  );
}
</style>
