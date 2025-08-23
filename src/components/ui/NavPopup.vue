<script setup>
import { defineEmits, defineProps } from 'vue'

const props = defineProps({
  show: Boolean,
})

const emit = defineEmits(['close'])
</script>

<template>
  <div
    v-if="show"
    class="absolute right-0 mt-2 w-28 bg-white backdrop-blur-3xl p-4 rounded-lg shadow-xl z-50 max-h-[70vh] overflow-y-auto"
  >
    <ul class="space-y-2">
      <li><a href="#about" class="hover:text-blue-500">About</a></li>
      <li><a href="#projects" class="hover:text-blue-500">Projects</a></li>
      <li><a href="#contact" class="hover:text-blue-500">Contact</a></li>
      <!-- contoh item tambahan biar panjang -->
      <li><a href="#blog" class="hover:text-blue-500">Blog</a></li>
      <li><a href="#services" class="hover:text-blue-500">Services</a></li>
      <li><a href="#team" class="hover:text-blue-500">Team</a></li>
      <li><a href="#careers" class="hover:text-blue-500">Careers</a></li>
      <li><a href="#faq" class="hover:text-blue-500">FAQ</a></li>
      <li><a href="#support" class="hover:text-blue-500">Support</a></li>
    </ul>
  </div>
</template>
