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
      <li><a href="#skills" class="hover:text-blue-500">Skills</a></li>
      <li><a href="#projects" class="hover:text-blue-500">Projects</a></li>
      <li><a href="#experiences" class="hover:text-blue-500">Experiences</a></li>
    </ul>
  </div>
</template>
