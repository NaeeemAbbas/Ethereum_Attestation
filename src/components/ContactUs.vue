<script setup>
import { ref } from 'vue';

const teamMembers = ref([
  {
    name: 'Leonid Beder',
    role: 'Lead Solidity & Security Engineer',
    description: 'Smart contracts engineer and auditor, security and OPSEC expert, ex-Machine Learning and Cryptography.',
    avatar: '/src/assets/Img1.png', // Placeholder for Bender-like avatar
    ringColor: 'border-blue-300', // Corresponding ring color
  },
  {
    name: 'Bryce Patrick',
    role: 'Protocol Growth & Adoption',
    description: 'Public goods builder & product person focusing on growth and adoption of EAS.',
    avatar: '/src/assets/Img2.jpg', // Placeholder for Bryce's avatar
    ringColor: 'border-purple-300', // Corresponding ring color
  },
  {
    name: 'Steve Dakh',
    role: 'Lead Full Stack Engineer',
    description: 'Founding team member of Ethereum, Rushwallet, and KryptoKit.',
    avatar: '/src/assets/Img3.jpg', // Placeholder for Steve's avatar
    ringColor: 'border-teal-300', // Corresponding ring color
  },
  {
    name: 'Dino Mark',
    role: 'Builder & Systems Designer',
    description: 'Early Ethereum contributor and systems designer for EAS.',
    avatar: '/src/assets/Img4.jpg', // Placeholder for Unicorn avatar
    ringColor: 'border-orange-300', // Corresponding ring color
  },
]);
</script>

<template>
  <div class="bg-white py-16 sm:py-24 px-4 sm:px-6 lg:px-8">
    <div class="max-w-7xl mx-auto">
      <div class="text-center mb-16 sm:mb-20">
        <h2 class="text-4xl sm:text-5xl font-extrabold text-gray-900 leading-tight mb-4">
          Come build with us.
        </h2>
        <p class="text-base sm:text-lg text-gray-600 max-w-2xl mx-auto">
          Ethereum Attestation Service is being built by the earliest of Ethereans and a diverse community of passionate builders.
        </p>
      </div>

      <div class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-4 gap-x-8 gap-y-12 sm:gap-y-16">
        <div v-for="(member, index) in teamMembers" :key="index" class="flex flex-col items-center text-center">
          <div :class="['w-32 h-32 rounded-full flex items-center justify-center p-1.5 mb-6', member.ringColor, 'border-4']">
            <img :src="member.avatar" :alt="member.name" class="w-full h-full object-cover rounded-full bg-gray-100" />
          </div>

          <h3 class="text-xl font-semibold text-gray-900 mb-1">
            {{ member.name }}
          </h3>
          <p class="text-blue-600 text-sm font-medium mb-3">
            {{ member.role }}
          </p>

          <p class="text-gray-600 text-sm max-w-xs">
            {{ member.description }}
          </p>
        </div>
      </div>
    </div>
  </div>
</template>

<style scoped>
/* No specific scoped styles are needed as Tailwind CSS handles everything */
</style>