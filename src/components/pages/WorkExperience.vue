<script setup>
import { ref } from 'vue'
import Calendar from '../icons/Calendar.vue'
import Trophy from '../icons/Trophy.vue'
import Institution from '../icons/Institution.vue'
import Award from '../icons/Award.vue'

const tabs = [
  'Work Experience',
  'Organizational Experience',
  'Achievement',
  'Certification & Training',
]
const activeTab = ref(tabs[0])
</script>

<template>
  <div class="flex flex-col items-center justify-center">
    <h1 class="font-bold text-4xl text-blue-500 mb-10">Experience</h1>

    <!-- Tabs -->
    <div class="flex gap-4 mb-8 border-b-2 border-gray-200">
      <button
        v-for="tab in tabs"
        :key="tab"
        @click="activeTab = tab"
        class="px-4 py-2 font-semibold transition"
        :class="
          activeTab === tab
            ? 'border-b-4 border-blue-500 text-blue-500'
            : 'text-gray-500 hover:text-blue-500'
        "
      >
        {{ tab }}
      </button>
    </div>

    <div class="container-work-experience">
      <div v-if="activeTab === 'Work Experience'" class="flex flex-col justify-center">
        <div class="flex flex-col mb-16 justify-between xl:flex-row gap-4">
          <div class="flex flex-col">
            <h1 class="font-extrabold text-2xl">Information Technology Developer</h1>
            <div class="flex-col justify-start mt-2">
              <p class="font-bold text-gray-500 text-xl">Internship</p>
              <p class="font-bold text-gray-500 text-xl">October 2024 - March 2025</p>
            </div>
          </div>
          <div class="flex flex-col pl-8 pt-0 pb-4 border-l-2 border-black">
            <div class="flex items-center gap-2 mb-2">
              <img src="@/assets/images/peruri-logo.jpg" alt="logo" width="60" />
              <h1 class="font-bold text-lg">Perum Percetakan Uang Republik Indonesia (PERURI)</h1>
            </div>
            <div class="max-w-lg mb-8">
              <ul class="space-y-1">
                <li class="flex items-start gap-3">
                  <span
                    class="flex h-8 w-8 items-center justify-center rounded-full bg-blue-100 text-blue-600 font-bold shadow"
                  >
                    1
                  </span>
                  <p class="text-gray-700 leading-relaxed">
                    Developed and enhanced internal web application interfaces to manage over 50
                    application data records
                  </p>
                </li>

                <li class="flex items-start gap-3">
                  <span
                    class="flex h-8 w-8 items-center justify-center rounded-full bg-green-100 text-green-600 font-bold shadow"
                  >
                    2
                  </span>
                  <p class="text-gray-700 leading-relaxed">
                    Coordinated and analyzed system requirements from multiple stakeholders,
                    delivering accurate specifications that streamlined the development process
                  </p>
                </li>

                <li class="flex items-start gap-3">
                  <span
                    class="flex h-8 w-8 items-center justify-center rounded-full bg-purple-100 text-purple-600 font-bold shadow"
                  >
                    3
                  </span>
                  <p class="text-gray-700 leading-relaxed">
                    Deployed over 3 applications using Docker, maintaining reliable performance and
                    standardized environments across deployment targets
                  </p>
                </li>

                <li class="flex items-start gap-3">
                  <span
                    class="flex h-8 w-8 items-center justify-center rounded-full bg-orange-100 text-orange-600 font-bold shadow"
                  >
                    4
                  </span>
                  <p class="text-gray-700 leading-relaxed">
                    Enhanced the web application by implementing more than 3 new features, improving
                    user efficiency, and optimizing workflow processes.
                  </p>
                </li>
              </ul>
            </div>

            <div class="flex gap-3">
              <div class="bg-blue-300 rounded-md px-1.5 py-1.5 flex justify-center items-center">
                <img src="@/assets/images/skills/docker.png" alt="logo" width="40" />
              </div>
              <div class="bg-blue-300 rounded-md px-1.5 py-1.5 flex justify-center items-center">
                <img src="@/assets/images/skills/laravel.png" alt="logo" width="40" />
              </div>
              <div class="bg-blue-300 rounded-md px-1.5 py-1.5 flex justify-center items-center">
                <img src="@/assets/images/skills/devops.png" alt="logo" width="40" />
              </div>
              <div class="bg-blue-300 rounded-md px-1.5 py-1.5 flex justify-center items-center">
                <img src="@/assets/images/skills/gitlab.png" alt="logo" width="40" />
              </div>
            </div>
          </div>
        </div>
        <div class="flex flex-col mb-16 justify-between xl:flex-row gap-4">
          <div class="flex-col">
            <h1 class="font-extrabold text-2xl">Frontend Web Developer</h1>
            <div class="flex-col justify-start mt-2">
              <p class="font-bold text-gray-500 text-xl">Internship</p>
              <p class="font-bold text-gray-500 text-xl">July 2024 - August 2024</p>
            </div>
          </div>
          <div class="flex flex-col pl-8 pt-0 pb-4 border-l-2 border-black">
            <div class="flex items-center gap-2 mb-2">
              <img src="@/assets/images/bts-log.png" alt="logo" width="60" />
              <h1 class="font-bold text-lg">PT Intersolusi Teknologi Asia (BTS.id)</h1>
            </div>
            <div class="max-w-lg mb-8">
              <ul class="space-y-1">
                <li class="flex items-start gap-3">
                  <span
                    class="flex h-8 w-8 items-center justify-center rounded-full bg-blue-100 text-blue-600 font-bold shadow"
                  >
                    1
                  </span>
                  <p class="text-gray-700 leading-relaxed">
                    Designed the system architecture and UI/UX flows, created system diagrams
                    including use case, ERD, and process flow diagrams, and implemented a
                    Trello-like task management application to ensure a smooth, user-friendly, and
                    functionally aligned interface
                  </p>
                </li>

                <li class="flex items-start gap-3">
                  <span
                    class="flex h-8 w-8 items-center justify-center rounded-full bg-green-100 text-green-600 font-bold shadow"
                  >
                    2
                  </span>
                  <p class="text-gray-700 leading-relaxed">
                    Developed the web application, enabling real-time data synchronization and
                    seamless communication with the backend
                  </p>
                </li>
              </ul>
            </div>
            <div class="flex gap-3">
              <div class="bg-blue-300 rounded-md px-1.5 py-1.5 flex justify-center items-center">
                <img src="@/assets/logo.svg" alt="logo" width="20" />
              </div>
              <div class="bg-blue-300 rounded-md px-1.5 py-1.5 flex justify-center items-center">
                <img src="@/assets/images/skills/express.png" alt="logo" width="20" />
              </div>
              <div class="bg-blue-300 rounded-md px-1.5 py-1.5 flex justify-center items-center">
                <img src="@/assets/images/skills/figma.png" alt="logo" width="20" />
              </div>
              <div class="bg-blue-300 rounded-md px-1.5 py-1.5 flex justify-center items-center">
                <img src="@/assets/images/skills/github.png" alt="logo" width="30" />
              </div>
              <div class="bg-blue-300 rounded-md px-1.5 py-1.5 flex justify-center items-center">
                <img src="@/assets/images/skills/websocket.svg" alt="logo" width="30" />
              </div>
            </div>
          </div>
        </div>
        <div class="flex flex-col mb-16 justify-between xl:flex-row gap-4">
          <div class="flex-col">
            <h1 class="font-extrabold text-2xl">Web Developer</h1>
            <div class="flex-col justify-start mt-2">
              <p class="font-bold text-gray-500 text-xl">Internship</p>
              <p class="font-bold text-gray-500 text-xl">August 2023 - September 2023</p>
            </div>
          </div>
          <div class="flex flex-col pl-8 pt-0 pb-4 border-l-2 border-black">
            <div class="flex items-center gap-2 mb-2">
              <img src="@/assets/images/bts-log.png" alt="logo" width="60" />
              <h1 class="font-bold text-lg">PT Intersolusi Teknologi Asia (BTS.id)</h1>
            </div>
            <div class="max-w-lg mb-8">
              <ul class="space-y-1">
                <li class="flex items-start gap-3">
                  <span
                    class="flex h-8 w-8 items-center justify-center rounded-full bg-blue-100 text-blue-600 font-bold shadow"
                  >
                    1
                  </span>
                  <p class="text-gray-700 leading-relaxed">
                    Analyzed requirements and designed the authentication module architecture,
                    outlining user flows and security specifications
                  </p>
                </li>

                <li class="flex items-start gap-3">
                  <span
                    class="flex h-8 w-8 items-center justify-center rounded-full bg-green-100 text-green-600 font-bold shadow"
                  >
                    2
                  </span>
                  <p class="text-gray-700 leading-relaxed">
                    Managed with the development team using collaboration tools for task management,
                    ensuring proper documentation, structured branching, and smooth collaboration
                    throughout the development cycle
                  </p>
                </li>
              </ul>
            </div>
            <div class="flex gap-3">
              <div class="bg-blue-300 rounded-md px-1.5 py-1.5 flex justify-center items-center">
                <img src="@/assets/logo.svg" alt="logo" width="20" />
              </div>
              <div class="bg-blue-300 rounded-md px-1.5 py-1.5 flex justify-center items-center">
                <img src="@/assets/images/skills/express.png" alt="logo" width="30" />
              </div>
              <div class="bg-blue-300 rounded-md px-1.5 py-1.5 flex justify-center items-center">
                <img src="@/assets/images/skills/gitlab.png" alt="logo" width="30" />
              </div>
              <div class="bg-blue-300 rounded-md px-1.5 py-1.5 flex justify-center items-center">
                <img src="@/assets/images/skills/figma.png" alt="logo" width="20" />
              </div>
            </div>
          </div>
        </div>
        <div class="flex flex-col mb-16 justify-between xl:flex-row gap-4">
          <div class="flex-col">
            <h1 class="font-extrabold text-2xl">Landing Page Builder (WordPress)</h1>
            <div class="flex-col justify-start mt-2">
              <p class="font-bold text-gray-500 text-xl">Internship</p>
              <p class="font-bold text-gray-500 text-xl">March 2024 - April 2024</p>
            </div>
          </div>
          <div class="flex flex-col pl-8 pt-0 pb-4 border-l-2 border-black">
            <div class="flex items-center gap-2 mb-2">
              <img src="@/assets/images/hapsoo-logo.jpg" alt="logo" width="60" />
              <h1 class="font-bold text-lg">Hapsoo</h1>
            </div>
            <div class="max-w-lg mb-8">
              <ul class="space-y-1">
                <li class="flex items-start gap-3">
                  <span
                    class="flex h-8 w-8 items-center justify-center rounded-full bg-blue-100 text-blue-600 font-bold shadow"
                  >
                    1
                  </span>
                  <p class="text-gray-700 leading-relaxed">
                    Gathered and analyzed requirements from multiple teams to design responsive,
                    conversion-focused landing pages aligned with campaign objectives
                  </p>
                </li>

                <li class="flex items-start gap-3">
                  <span
                    class="flex h-8 w-8 items-center justify-center rounded-full bg-green-100 text-green-600 font-bold shadow"
                  >
                    2
                  </span>
                  <p class="text-gray-700 leading-relaxed">
                    Created wireframes, determined content structure, and collaborated with
                    cross-functional teams from over 2 divisions, ensuring visual and functional
                    consistency across deliverables
                  </p>
                </li>
              </ul>
            </div>
            <div class="flex gap-3">
              <div class="bg-blue-300 rounded-md px-1.5 py-1.5 flex justify-center items-center">
                <img src="@/assets/images/skills/wordpress.png" alt="logo" width="20" />
              </div>
              <div class="bg-blue-300 rounded-md px-1.5 py-1.5 flex justify-center items-center">
                <img src="@/assets/images/skills/elementor.png" alt="logo" width="20" />
              </div>
            </div>
          </div>
        </div>
      </div>
      <div v-if="activeTab === 'Organizational Experience'" class="flex flex-col justify-center">
        <div class="flex flex-col mb-16 justify-between xl:flex-row gap-4">
          <div class="flex">
            <h1 class="font-extrabold text-2xl">Coordinator - Event Management Crew</h1>
          </div>
          <div class="flex flex-col pl-8 pt-0 pb-4 border-l-2 border-black">
            <div class="flex items-center gap-2 mb-2">
              <institution />
              <h1 class="font-bold text-lg">Generation of Information System (GENESIS) 2023</h1>
            </div>
            <div class="max-w-lg mb-8">
              <ul class="space-y-1">
                <li class="flex items-start gap-3">
                  <span
                    class="flex h-8 w-8 items-center justify-center rounded-full bg-blue-100 text-blue-600 font-bold shadow"
                  >
                    1
                  </span>
                  <p class="text-gray-700 leading-relaxed">
                    Led a team of 40 members, increasing efficiency and ensuring 100% of pre-event
                    deliverables were completed ahead of schedule
                  </p>
                </li>

                <li class="flex items-start gap-3">
                  <span
                    class="flex h-8 w-8 items-center justify-center rounded-full bg-green-100 text-green-600 font-bold shadow"
                  >
                    2
                  </span>
                  <p class="text-gray-700 leading-relaxed">
                    Designed and structured over 10 events, delivering creative and well-detailed
                    programs with 100% adherence to the planned timeline
                  </p>
                </li>

                <li class="flex items-start gap-3">
                  <span
                    class="flex h-8 w-8 items-center justify-center rounded-full bg-purple-100 text-purple-600 font-bold shadow"
                  >
                    3
                  </span>
                  <p class="text-gray-700 leading-relaxed">
                    Successfully managed the flow of events, overseeing the implementation of
                    activities without disruptions, resulting in a seamless experience for over 200
                    participants
                  </p>
                </li>
              </ul>
            </div>
            <div class="flex flex-wrap gap-3 max-w-[520px] overflow-hidden">
              <div class="bg-blue-300 rounded-md px-1.5 py-1.5 flex justify-center items-center">
                <p class="font-semibold">Leadership</p>
              </div>
              <div class="bg-blue-300 rounded-md px-1.5 py-1.5 flex justify-center items-center">
                <p class="font-semibold">Event organization</p>
              </div>
              <div class="bg-blue-300 rounded-md px-1.5 py-1.5 flex justify-center items-center">
                <p class="font-semibold">Team coordination</p>
              </div>
              <div class="bg-blue-300 rounded-md px-1.5 py-1.5 flex justify-center items-center">
                <p class="font-semibold">Project management</p>
              </div>
              <div class="bg-blue-300 rounded-md px-1.5 py-1.5 flex justify-center items-center">
                <p class="font-semibold">Problem-solving</p>
              </div>
            </div>
          </div>
        </div>
        <div class="flex flex-col mb-16 justify-between xl:flex-row gap-4">
          <div class="flex">
            <h1 class="font-extrabold text-2xl">External Division</h1>
          </div>
          <div class="flex flex-col pl-8 pt-0 pb-4 border-l-2 border-black">
            <div class="flex items-center gap-2 mb-2">
              <institution />
              <h1 class="font-bold text-lg">Persatuan Olahraga Sistem Informasi</h1>
            </div>
            <div class="max-w-lg mb-8">
              <ul class="space-y-1">
                <li class="flex items-start gap-3">
                  <span
                    class="flex h-8 w-8 items-center justify-center rounded-full bg-blue-100 text-blue-600 font-bold shadow"
                  >
                    1
                  </span>
                  <p class="text-gray-700 leading-relaxed">
                    Researched and secured over 5 sports competition opportunities, coordinating
                    team selection, training schedules, and logistics to ensure optimal preparation
                    and competitive performance
                  </p>
                </li>

                <li class="flex items-start gap-3">
                  <span
                    class="flex h-8 w-8 items-center justify-center rounded-full bg-green-100 text-green-600 font-bold shadow"
                  >
                    2
                  </span>
                  <p class="text-gray-700 leading-relaxed">
                    Organized and executed 3 sports tournaments from concept to completion, managing
                    event planning, scheduling, and on-site operations, resulting in high
                    participation and positive feedback from attendees
                  </p>
                </li>
              </ul>
            </div>
            <div class="flex flex-wrap gap-3 max-w-[520px] overflow-hidden">
              <div class="bg-blue-300 rounded-md px-1.5 py-1.5 flex justify-center items-center">
                <p class="font-semibold">Event organization</p>
              </div>
              <div class="bg-blue-300 rounded-md px-1.5 py-1.5 flex justify-center items-center">
                <p class="font-semibold">Team coordination</p>
              </div>
              <div class="bg-blue-300 rounded-md px-1.5 py-1.5 flex justify-center items-center">
                <p class="font-semibold">Collaboration</p>
              </div>
              <div class="bg-blue-300 rounded-md px-1.5 py-1.5 flex justify-center items-center">
                <p class="font-semibold">Communication</p>
              </div>
            </div>
          </div>
        </div>
        <div class="flex flex-col mb-16 justify-between xl:flex-row gap-4">
          <div class="flex">
            <h1 class="font-extrabold text-2xl">Administration Division</h1>
          </div>
          <div class="flex flex-col pl-8 pt-0 pb-4 border-l-2 border-black">
            <div class="flex items-center gap-2 mb-2">
              <institution />
              <h1 class="font-bold text-lg">Forum Institusi Layanan Bahasa</h1>
            </div>
            <div class="max-w-lg mb-8">
              <ul class="space-y-1">
                <li class="flex items-start gap-3">
                  <span
                    class="flex h-8 w-8 items-center justify-center rounded-full bg-blue-100 text-blue-600 font-bold shadow"
                  >
                    1
                  </span>
                  <p class="text-gray-700 leading-relaxed">
                    Coordinated over 15 administrative activities within 1 month, including
                    scheduling, workflow planning, and task distribution
                  </p>
                </li>

                <li class="flex items-start gap-3">
                  <span
                    class="flex h-8 w-8 items-center justify-center rounded-full bg-green-100 text-green-600 font-bold shadow"
                  >
                    2
                  </span>
                  <p class="text-gray-700 leading-relaxed">
                    Managed over 100 documents and attendee data for various events, ensuring the
                    accuracy and availability of information for the team and stakeholders
                  </p>
                </li>
              </ul>
            </div>
            <div class="flex flex-wrap gap-3 max-w-[520px] overflow-hidden">
              <div class="bg-blue-300 rounded-md px-1.5 py-1.5 flex justify-center items-center">
                <p class="font-semibold">Detail orientation</p>
              </div>
              <div class="bg-blue-300 rounded-md px-1.5 py-1.5 flex justify-center items-center">
                <p class="font-semibold">Document & data management</p>
              </div>
              <div class="bg-blue-300 rounded-md px-1.5 py-1.5 flex justify-center items-center">
                <p class="font-semibold">Collaboration</p>
              </div>
              <div class="bg-blue-300 rounded-md px-1.5 py-1.5 flex justify-center items-center">
                <p class="font-semibold">Administrative Management</p>
              </div>
              <div class="bg-blue-300 rounded-md px-1.5 py-1.5 flex justify-center items-center">
                <p class="font-semibold">Workflow planning</p>
              </div>
            </div>
          </div>
        </div>
      </div>
      <div v-if="activeTab === 'Achievement'" class="flex flex-col justify-center">
        <div class="grid grid-cols-1 sm:grid-cols-2 gap-6">
          <div class="bg-white shadow-lg rounded-2xl p-6">
            <div class="flex justify-between items-start">
              <div>
                <div class="flex gap-1 items-center mb-2">
                  <Trophy class="w-4 h-4" />
                  <p
                    class="text-md font-semibold text-gray-700 bg-green-400 rounded-md px-1.5 py-0"
                  >
                    National
                  </p>
                </div>
                <h3 class="text-lg font-semibold mb-2 w-full">
                  2nd Winner Business Plan Competition at Startup Ideas 2022
                </h3>
              </div>
              <div class="flex gap-2 w-1/3 text-lg font-semibold text-gray-400 justify-end">
                <div class="flex items-center gap-2">
                  <Calendar class="w-5 h-5" />
                  <p>Nov 2022</p>
                </div>
              </div>
            </div>
            <div class="max-w-lg mb-8">
              <ul class="space-y-1">
                <li class="flex items-start gap-3">
                  <span
                    class="flex h-8 w-8 items-center justify-center rounded-full bg-blue-100 text-blue-600 font-bold shadow"
                  >
                    1
                  </span>
                  <p class="text-gray-700 leading-relaxed">
                    Led a team of 5 members in developing a startup concept and business model
                    focused on Digital Solution
                  </p>
                </li>

                <li class="flex items-start gap-3">
                  <span
                    class="flex h-8 w-8 items-center justify-center rounded-full bg-green-100 text-green-600 font-bold shadow"
                  >
                    2
                  </span>
                  <p class="text-gray-700 leading-relaxed">
                    Conducted market research and feasibility analysis, validating target audience
                    and competitive positioning
                  </p>
                </li>

                <li class="flex items-start gap-3">
                  <span
                    class="flex h-8 w-8 items-center justify-center rounded-full bg-purple-100 text-purple-600 font-bold shadow"
                  >
                    3
                  </span>
                  <p class="text-gray-700 leading-relaxed">
                    Designed a pitch deck and financial projection to present to judges and
                    potential stakeholders
                  </p>
                </li>

                <li class="flex items-start gap-3">
                  <span
                    class="flex h-8 w-8 items-center justify-center rounded-full bg-orange-100 text-orange-600 font-bold shadow"
                  >
                    4
                  </span>
                  <p class="text-gray-700 leading-relaxed">
                    Strengthened skills in entrepreneurship, analytical thinking, and persuasive
                    communication
                  </p>
                </li>
              </ul>
            </div>
          </div>
          <div class="bg-white shadow-lg rounded-2xl p-6">
            <div class="flex justify-between items-start">
              <div>
                <div class="flex gap-1 items-center mb-2">
                  <Trophy class="w-4 h-4" />
                  <p
                    class="text-md font-semibold text-gray-700 bg-green-400 rounded-md px-1.5 py-0"
                  >
                    National
                  </p>
                </div>
                <h3 class="text-lg font-semibold mb-2 w-full">
                  3rd Business Plan Competition at Accounting Information System 2023
                </h3>
              </div>
              <div class="flex gap-2 w-1/3 text-lg font-semibold text-gray-400 justify-end">
                <div class="flex items-center gap-2">
                  <Calendar class="w-5 h-5" />
                  <p>Jan 2023</p>
                </div>
              </div>
            </div>
            <div class="max-w-lg mb-8">
              <ul class="space-y-1">
                <li class="flex items-start gap-3">
                  <span
                    class="flex h-8 w-8 items-center justify-center rounded-full bg-blue-100 text-blue-600 font-bold shadow"
                  >
                    1
                  </span>
                  <p class="text-gray-700 leading-relaxed">
                    Led a team of 3 members in developing a startup concept and business model
                    focused on Digital Solution
                  </p>
                </li>

                <li class="flex items-start gap-3">
                  <span
                    class="flex h-8 w-8 items-center justify-center rounded-full bg-green-100 text-green-600 font-bold shadow"
                  >
                    2
                  </span>
                  <p class="text-gray-700 leading-relaxed">
                    Conducted system and business process analysis, identifying pain points and
                    proposing innovative solutions to improve efficiency and scalability
                  </p>
                </li>

                <li class="flex items-start gap-3">
                  <span
                    class="flex h-8 w-8 items-center justify-center rounded-full bg-purple-100 text-purple-600 font-bold shadow"
                  >
                    3
                  </span>
                  <p class="text-gray-700 leading-relaxed">
                    Designed a pitch deck and financial projection to present to judges and
                    potential stakeholders
                  </p>
                </li>

                <li class="flex items-start gap-3">
                  <span
                    class="flex h-8 w-8 items-center justify-center rounded-full bg-orange-100 text-orange-600 font-bold shadow"
                  >
                    4
                  </span>
                  <p class="text-gray-700 leading-relaxed">
                    Showcased leadership, business analysis, and presentation skills, achieving 3rd
                    place in a highly competitive competition
                  </p>
                </li>
              </ul>
            </div>
          </div>
        </div>
      </div>
      <div v-if="activeTab === 'Certification & Training'" class="flex flex-col justify-center">
        <div class="grid grid-cols-1 sm:grid-cols-2 gap-6">
          <div class="bg-white shadow-lg rounded-2xl p-6">
            <div>
              <div class="flex gap-1 items-center mb-2">
                <Award class="w-4 h-4" />
                <p class="text-md font-semibold text-gray-700 bg-blue-400 rounded-md px-1.5 py-0">
                  Certification
                </p>
              </div>
              <h3 class="text-lg font-semibold mb-2">Certificied System Analyst (CSA)</h3>
              <div class="text-gray-400 flex items-center gap-2">
                <Institution class="w-4 h-4" />
                <h2 class="text-lg font-semibold">Badan Nasional Sertifikasi Profesi (BNSP)</h2>
              </div>
            </div>
            <p class="text-gray-600">Validated competency in requirements analysis, system design, and documentation based on national professional standards.</p>
          </div>
          <div class="bg-white shadow-lg rounded-2xl p-6">
            <div>
              <div class="flex gap-1 items-center mb-2">
                <Award class="w-4 h-4" />
                <p class="text-md font-semibold text-gray-700 bg-orange-400 rounded-md px-1.5 py-0">
                  Training
                </p>
              </div>
              <h3 class="text-lg font-semibold mb-2">Source Code Management & DevSecOps</h3>
              <div class="text-gray-400 flex items-center gap-2">
                <Institution class="w-4 h-4" />
                <h2 class="text-lg font-semibold">Narada Code</h2>
              </div>
            </div>
            <p class="text-gray-600">Hands-on training in version control, CI/CD pipelines, and secure DevOps practices.</p>
          </div>
          <div class="bg-white shadow-lg rounded-2xl p-6">
            <div>
              <div class="flex gap-1 items-center mb-2">
                <Award class="w-4 h-4" />
                <p class="text-md font-semibold text-gray-700 bg-orange-400 rounded-md px-1.5 py-0">
                  Training
                </p>
              </div>
              <h3 class="text-lg font-semibold mb-2">
                Mobile Application Development (Flutter) & Front-end App (React JS)
              </h3>
              <div class="text-gray-400 flex items-center gap-2">
                <Institution class="w-4 h-4" />
                <h2 class="text-lg font-semibold">Kata Suhu Kita</h2>
              </div>
            </div>
            <p class="text-gray-600">Learned to build cross-platform apps with Flutter and develop responsive frontends with React JS.</p>
          </div>
          <div class="bg-white shadow-lg rounded-2xl p-6">
            <div>
              <div class="flex gap-1 items-center mb-2">
                <Award class="w-4 h-4" />
                <p class="text-md font-semibold text-gray-700 bg-orange-400 rounded-md px-1.5 py-0">
                  Training
                </p>
              </div>
              <h3 class="text-lg font-semibold mb-2">
                Full Stack MEVN (MongoDB, Express, Vue, and Node JS)
              </h3>
              <div class="text-gray-400 flex items-center gap-2">
                <Institution class="w-4 h-4" />
                <h2 class="text-lg font-semibold">Code Politan</h2>
              </div>
            </div>
            <p class="text-gray-600">Trained in end-to-end web application development using the MEVN stack.</p>
          </div>
          <div class="bg-white shadow-lg rounded-2xl p-6">
            <div>
              <div class="flex gap-1 items-center mb-2">
                <Award class="w-4 h-4" />
                <p class="text-md font-semibold text-gray-700 bg-blue-400 rounded-md px-1.5 py-0">
                  Certification
                </p>
              </div>
              <h3 class="text-lg font-semibold mb-2">Certified SCRUM Master</h3>
              <div class="text-gray-400 flex items-center gap-2">
                <Institution class="w-4 h-4" />
                <h2 class="text-lg font-semibold">Certiprof</h2>
              </div>
            </div>
            <p class="text-gray-600">Certified in Agile project management and SCRUM framework for effective team collaboration and iterative development.</p>
          </div>
          <div class="bg-white shadow-lg rounded-2xl p-6">
            <div>
              <div class="flex gap-1 items-center mb-2">
                <Award class="w-4 h-4" />
                <p class="text-md font-semibold text-gray-700 bg-blue-400 rounded-md px-1.5 py-0">
                  Certification
                </p>
              </div>
              <h3 class="text-lg font-semibold mb-2">
                Certified SCM500 - Processes in Procurement
              </h3>
              <div class="text-gray-400 flex items-center gap-2">
                <Institution class="w-4 h-4" />
                <h2 class="text-lg font-semibold">SAP</h2>
              </div>
            </div>
            <p class="text-gray-600">Demonstrated understanding of SAP procurement processes, including purchasing, requisition, and supplier management.</p>
          </div>
          <div class="bg-white shadow-lg rounded-2xl p-6">
            <div>
              <div class="flex gap-1 items-center mb-2">
                <Award class="w-4 h-4" />
                <p class="text-md font-semibold text-gray-700 bg-blue-400 rounded-md px-1.5 py-0">
                  Certification
                </p>
              </div>
              <h3 class="text-lg font-semibold mb-2">
                Certified AC10 - Business Processes in Financial Accounting
              </h3>
              <div class="text-gray-400 flex items-center gap-2">
                <Institution class="w-4 h-4" />
                <h2 class="text-lg font-semibold">SAP</h2>
              </div>
            </div>
            <p class="text-gray-600">Certified in SAP financial accounting processes, covering accounts management and reporting.</p>
          </div>
          <div class="bg-white shadow-lg rounded-2xl p-6">
            <div>
              <div class="flex gap-1 items-center mb-2">
                <Award class="w-4 h-4" />
                <p class="text-md font-semibold text-gray-700 bg-blue-400 rounded-md px-1.5 py-0">
                  Certification
                </p>
              </div>
              <h3 class="text-lg font-semibold mb-2">Certified SAP01 - SAP Overview</h3>
              <div class="text-gray-400 flex items-center gap-2">
                <Institution class="w-4 h-4" />
                <h2 class="text-lg font-semibold">SAP</h2>
              </div>
            </div>
            <p class="text-gray-600">Gained foundational knowledge of SAP modules, integration, and business process applications.</p>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<style setup>
.container-work-experience {
  width: 55%;
}
</style>
