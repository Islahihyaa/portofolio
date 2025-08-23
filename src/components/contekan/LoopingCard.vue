<template>
    <div class="relative w-full overflow-hidden bg-gray-100 py-10">
      <div class="flex space-x-6 animate-marquee">
        <!-- Loop komentar dua kali untuk membuat efek looping -->
        <div
          v-for="(comment, index) in [...comments, ...comments]"
          :key="index"
          class="bg-white rounded-xl shadow-md p-6 min-w-[300px] max-w-[400px]"
        >
          <button class="float-right text-xl">❌</button>
          <h2 class="font-bold text-lg">@{{ comment.username }}</h2>
          <p class="text-gray-600">{{ comment.text }}</p>
        </div>
      </div>
    </div>
  </template>
  
  <script setup>
  import { ref } from "vue";
  
  const comments = ref([
    { username: "darronj", text: "This is the second most valuable feature in my opinion!" },
    { username: "YourBuddyConner", text: "@HasuraHQ has gotten so good the last couple years" },
    { username: "namoscato", text: "We believe @HasuraHQ is the future of #GraphQL API development." },
    { username: "devguy", text: "I love using Hasura for my projects. It saves so much time!" },
  ]);
  </script>
  
  <style>
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
    animation: marquee 10s linear infinite;
    white-space: nowrap;
    width: max-content;
  }
  </style>
  