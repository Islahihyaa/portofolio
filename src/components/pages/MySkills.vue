<script setup>
import { ref } from 'vue'
import Vue from '@/assets/logo.svg'
import React from '@/assets/images/logo/1.png'
import ReactNative from '@/assets/images/logo/2.png'
import JS from '@/assets/images/logo/3.png'
import ExpressJS from '@/assets/images/logo/4.png'
import NodeJS from '@/assets/images/logo/5.png'
import Laravel from '@/assets/images/logo/15.png'
import DevSecOps from '@/assets/images/logo/16.png'
import Docker from '@/assets/images/logo/9.png'
import Jira from '@/assets/images/logo/7.png'
import Figma from '@/assets/images/logo/8.png'
import ClickUp from '@/assets/images/logo/10.png'
import GitLab from '@/assets/images/logo/11.png'
import RabbitMQ from '@/assets/images/logo/12.png'
import MongoDB from '@/assets/images/logo/13.png'
import MySQL from '@/assets/images/logo/14.png'
import WebSocket from '@/assets/images/skills/websocket.svg'
import Pinia from '@/assets/images/logo/6.png'
import Prisma from '@/assets/images/logo/17.png'


const skills = ref([
  {
    name: 'VUE',
    img: Vue,
  },
  {
    name: 'REACT',
    img: React,
  },
  {
    name: 'REACT NATIVE',
    img: ReactNative,
  },
  {
    name: 'JAVASCRIPT',
    img: JS,
  },
  {
    name: 'EXPRESS JS',
    img: ExpressJS,
  },
  {
    name: 'NODE JS',
    img: NodeJS,
  },
  {
    name: 'LARAVEL',
    img: Laravel,
  },
  {
    name: 'DevSecOps',
    img: DevSecOps,
  },
  {
    name: 'JIRA',
    img: Jira,
  },
  {
    name: 'DOCKER',
    img: Docker,
  },
  {
    name: 'FIGMA',
    img: Figma,
  },
  {
    name: 'CLICK UP',
    img: ClickUp,
  },
  {
    name: 'GITLAB',
    img: GitLab,
  },
  {
    name: 'RABBIT MQ',
    img: RabbitMQ,
  },
  {
    name: 'MONGODB',
    img: MongoDB,
  },
  {
    name: 'MYSQL',
    img: MySQL,
  },
  {
    name: 'WEB SOCKET',
    img: WebSocket,
  },
  {
    name: 'PINIA',
    img: Pinia,
  },
  {
    name: 'PRISMA',
    img: Prisma,
  },
])
</script>

<template>
  <div class="flex flex-col items-center justify-center">
    <h1 class="font-bold text-4xl text-blue-500 mb-10">My Skills</h1>
    <div class="container">
      <div class="flex flex-wrap justify-center gap-4">
        <!-- component -->
        <div
          v-for="(skill, index) in skills"
          :key="index"
          class="fade-up flex justify-center items-center max-w-sm bg-blue-200 rounded-xl shadow-lg overflow-hidden hover:shadow-xl transition-all w-36 h-32"
        >
          <div class="p-5 space-y-4">
            <div class="flex flex-col justify-center items-center">
              <img :src="skills[index].img" :alt="skill.name" width="50" />
              <h3 class="text-md font-medium text-center text-gray-900 mt-2">{{ skill.name }}</h3>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<style scoped>
.container {
  width: 70%;
}

@keyframes appear {
  from {
    opacity: 0;
    clip-path: inset(100% 0 0 0);
  }
  to {
    opacity: 1;
    clip-path: inset(0 0 0 0);
  }
}

.fade-up {
  animation: appear linear;
  animation-timeline: view();
  animation-range: entry 0% cover 35%;
}
</style>
