<script setup>
import { ref, computed } from 'vue'; // Import computed
import img1 from '../assets/img1.png'
import img2 from '../assets/img2.jpg'
import img3 from '../assets/img3.jpg'
import img4 from '../assets/img4.jpg'
import img5 from '../assets/img5.jpg'

// Dummy data for content cards
const allContentCards = ref([ // Renamed to avoid conflict
  {
    type: 'video',
    thumbnail: img2, // Dummy image for videos
    title: 'Ethereum Attestation Service: Unlocking Decentralized Identity',
    author: 'Bankless',
    role: 'Podcaster',
  },
  {
    type: 'video',
    thumbnail: img3, // Dummy image for videos
    title: 'Ethereum Attestation Service (EAS) Explainer',
    author: 'Vaibhav Saini',
    role: 'Co-Founder, OpenSea Pro',
  },
  {
    type: 'video',
    thumbnail: img4,
    title: 'ETHGlobal Paris - Speedrun EAS',
    author: 'Bryce Patrick',
    role: 'Core Team at EAS',
  },
  {
    type: 'video',
    thumbnail: img5, // Dummy image for videos
    title: 'Crafting the New Web of Trust & Digital Credibility',
    author: 'Chaskin OnChain',
    role: 'Contributor',
  },
  {
    type: 'article',
    thumbnail: img1, // Placeholder image for articles
    title: 'Supercharging Account Abstraction with Attestations',
    author: 'Bryce Patrick',
    role: 'Core Team at EAS',
  },
  {
    type: 'article',
    thumbnail: img1, // Placeholder image for articles
    title: 'ELIS Ethereum Attestation Service (EAS) - Why You Should Care',
    author: 'Ryan Yi',
    role: 'Coinbase Ventures',
  },
]);

// Computed properties to separate videos and articles
const videoCards = computed(() =>
  allContentCards.value.filter(card => card.type === 'video')
);

const articleCards = computed(() =>
  allContentCards.value.filter(card => card.type === 'article')
);
</script>

<template>
  <div class="bg-white py-12 sm:py-16 px-4 sm:px-6 lg:px-8 mx-auto max-w-6xl">
    <div class="max-w-7xl mx-auto">
      <div class="text-center mb-10 sm:mb-12">
        <h1 class="text-4xl sm:text-5xl font-extrabold text-gray-900 leading-tight mb-3">
          Community Content
        </h1>
        <p class="text-base sm:text-lg text-gray-600 max-w-2xl mx-auto">
          Explore videos and articles created by people in the EAS community.
        </p>
      </div>

      <h2 class="text-3xl sm:text-4xl font-bold text-gray-800 mb-6 mt-10">Videos</h2>
      <div class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-3 xl:grid-cols-4 gap-6 sm:gap-8 mb-12">
        <div v-for="(card, index) in videoCards" :key="'video-' + index"
             class="bg-white rounded-lg shadow-md border border-gray-200 overflow-hidden
                    transition-transform duration-300 ease-in-out hover:scale-103 hover:shadow-lg cursor-pointer">
          <div class="relative w-full aspect-video bg-gray-100 flex items-center justify-center ">
            <img :src="card.thumbnail" :alt="card.title" class="w-full h-full object-cover"
                 onerror="this.onerror=null; this.src='https://placehold.co/400x225/cccccc/333333?text=Image+Error';"
            />
            <span v-if="card.type === 'video'" class="absolute bottom-2 right-2 bg-black bg-opacity-75 text-white text-xs px-2 py-1 rounded-full">
              Video
            </span>
          </div>
          <div class="p-4">
            <h3 class="text-lg font-semibold text-gray-800 mb-2 leading-tight">
              {{ card.title }}
            </h3>
            <div class="flex items-center text-sm text-gray-500">
              <div class="w-8 h-8 rounded-full bg-gray-200 flex-shrink-0 mr-3 overflow-hidden">
                <img src="https://placehold.co/32x32/c0d9ed/000000?text=Avatar" alt="Author Avatar" class="w-full h-full object-cover"
                     onerror="this.onerror=null; this.src='https://placehold.co/32x32/cccccc/333333?text=A';" />
              </div>
              <div>
                <p class="font-medium text-gray-700">{{ card.author }}</p>
                <p class="text-xs text-gray-500">{{ card.role }}</p>
              </div>
            </div>
          </div>
        </div>
      </div>

      <h2 class="text-3xl sm:text-4xl font-bold text-gray-800 mb-6 mt-10">Articles</h2>
      <div class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-2 gap-8 sm:gap-12"> <div v-for="(card, index) in articleCards" :key="'article-' + index"
             class="bg-white rounded-lg shadow-md border border-gray-200 overflow-hidden
                    transition-transform duration-300 ease-in-out hover:scale-103 hover:shadow-lg cursor-pointer">
          <div class="relative w-full aspect-video bg-gray-100 flex items-center justify-center ">
            <img :src="card.thumbnail" :alt="card.title" class="w-full h-full object-cover"
                 onerror="this.onerror=null; this.src='https://placehold.co/400x225/cccccc/333333?text=Image+Error';"
            />
            <span v-if="card.type === 'article'" class="absolute bottom-2 right-2 bg-blue-600 bg-opacity-75 text-white text-xs px-2 py-1 rounded-full">
              Article
            </span>
          </div>
          <div class="p-4">
            <h3 class="text-lg font-semibold text-gray-800 mb-2 leading-tight">
              {{ card.title }}
            </h3>
            <div class="flex items-center text-sm text-gray-500">
              <div class="w-8 h-8 rounded-full bg-gray-200 flex-shrink-0 mr-3 overflow-hidden">
                <img src="https://placehold.co/32x32/c0d9ed/000000?text=Avatar" alt="Author Avatar" class="w-full h-full object-cover"
                     onerror="this.onerror=null; this.src='https://placehold.co/32x32/cccccc/333333?text=A';" />
              </div>
              <div>
                <p class="font-medium text-gray-700">{{ card.author }}</p>
                <p class="text-xs text-gray-500">{{ card.role }}</p>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<style scoped>
/* No specific scoped styles are needed as Tailwind CSS handles everything */
</style>