<script setup>
import { ref } from 'vue'

const comments = ref([
  { username: 'darronj', text: 'This is the second most valuable feature in my opinion!' },
  {
    username: 'YourBuddyConner',
    text: ', @HasuraHQ has gotten so good the last couple years, @HasuraHQ has gotten so good the last couple years',
  },
  {
    username: 'namoscato',
    text: 'We believe @HasuraHQ is the future of #GraphQL API development.',
  },
  { username: 'devguy', text: 'I love using Hasura for my projects. It saves so much time!' },
])
</script>

<template>
  <section class="flex flex-col items-center justify-center">
    <div class="container flex justify-center gap-16">
      <div class="flex flex-col justify-start items-end w-1/3">
        <div class="text-start">
          <div class="bg-gray-400 rounded-2xl w-96 h-60 mb-6"></div>
          <h1 class="font-bold text-2xl px-6">Created by Islahihya</h1>
        </div>
      </div>
      <div class="flex w-1/2 h-full gap-4 relative overflow-hidden py-10">
        <div class="flex animate-marquee">
          <div
            v-for="(comment, index) in [...comments, ...comments]"
            :key="index"
            class="w-auto flex-1"
          >
            <div class="bg-gray-200 p-4 rounded-2xl mx-2 max-w-lg">
              <img src="@/assets/logo.svg" alt="" width="40" />
              <h2 class="font-bold mb-3">{{ comment.username }}</h2>
              <p>
                {{ comment.text }}
              </p>
            </div>
          </div>
        </div>
        <div
          class="absolute left-0 top-0 h-full w-20 bg-gradient-to-r from-white via-gray-100/30 to-transparent pointer-events-none"
        ></div>
      </div>
    </div>
  </section>
</template>

<style scoped>
@keyframes marquee {
  0% {
    transform: translateX(0);
  }
  100% {
    transform: translateX(-50%);
  }
}

.animate-marquee {
  display: flex;
  animation: marquee 20s linear infinite;
  white-space: nowrap;
  width: max-content;
}
</style>
