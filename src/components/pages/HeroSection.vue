<script setup>
import Button from '../ui/Button.vue'
import Pattern from '../icons/Pattern.vue'

const biodata = {
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
}
</script>

<template>
  <section class="relative">
    <div
      class="container mx-auto flex flex-col lg:flex-row items-center text-center lg:text-left gap-6 lg:gap-20 py-12"
    >
      <div class="md:w-2/5 flex justify-center mt-10 lg:mt-0">
        <img
          src="@/assets/images/my-foto-bg.png"
          alt="Profile picture of Islahihya Muhammad Jel Shibyan"
          class="rounded-xl border-y-4 border-blue-400 shadow-lg"
          width="400"
          height="400"
        />
      </div>

      <article class="md:w-3/5 flex flex-col justify-center">
        <header>
          <h3 class="text-2xl font-bold text-blue-400 mb-3">Hello, I'm</h3>
          <h1 class="text-5xl md:text-6xl font-bold leading-tight">
            <em class="text-header-gradient">Islahihya</em> Muhammad <br />
            Jel <em class="text-header-gradient">Shibyan</em>
          </h1>
        </header>

        <h2 class="text-lg md:text-xl font-semibold my-4 text-gray-700">
          {{ biodata.interest.join(' | ') }}
        </h2>

        <p class="py-4 text-gray-600 font-medium leading-relaxed">
          {{ biodata.summary }}
        </p>

        <div class="mt-4">
          <a
            href="https://wa.me/+6288215419786"
            target="_blank"
            rel="noopener noreferrer"
            aria-label="Connect with me on WhatsApp"
          >
            <Button>Connect Now</Button>
          </a>
        </div>
      </article>
    </div>

    <!-- Decorative Pattern -->
    <Pattern class="absolute bottom-0 right-0 opacity-20" />
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
