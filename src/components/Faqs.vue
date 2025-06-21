<script setup>
// Data for the cards
const cards = [
  { title: "Identity", description: "Digital, physical, agent identities." },
  { title: "Statements", description: "Things you say online." },
  { title: "Asset ownership", description: "What you own, like a car or house." },
  { title: "Votes", description: "What you care about." },
  { title: "Reputation", description: "Your trust and credibility." },
  { title: "Credentials", description: "Your skills and badges." },
  { title: "Eligibilities", description: "What you have access to." },
  { title: "Financial status", description: "Credit scores and financial health." },
  { title: "Digital signatures", description: "Verified signatures on chain." },
  { title: "Provenance", description: "The origination of anything." },
];
</script>

<template>
  <!-- Main Container: Centered, responsive padding, light blue background -->
  <div class="bg-blue-50 py-8 px-4 sm:px-6 lg:px-8 flex flex-col items-center">
    <!-- Content Wrapper: Controls max width and horizontal centering -->
    <div class="mx-auto max-w-6xl w-full">

      <!-- Header Section: Title, Description, and Button -->
      <!-- Flex layout: column on small screens, row on medium screens -->
      <div class="flex flex-col md:flex-row items-center md:justify-between mb-8 md:mb-12">
        <!-- Title and Description Block -->
        <div class="text-center md:text-left mb-6 md:mb-0 md:w-auto flex-shrink-0">
          <h1 class="text-3xl sm:text-4xl lg:text-5xl font-bold text-gray-800 leading-tight mb-2">
            Attest to anything.
          </h1>
          <p class="mt-2 text-base sm:text-lg text-gray-600 max-w-sm sm:max-w-md mx-auto md:mx-0">
            Easily create your own schemas for your unique use case or explore a few created by the community.
          </p>
        </div>

        <!-- Explore Button -->
        <div class="flex-shrink-0 mt-4 md:mt-0">
          <button class="px-8 py-3 text-base font-medium text-blue-600 border border-blue-600 rounded-lg hover:bg-blue-100 transition duration-300 ease-in-out shadow-sm">
            Explore Ideas
          </button>
        </div>
      </div>

      <!-- Grid of Cards -->
      <!-- Responsive grid: 1 column by default, 2 on small, 3 on medium, 4 on large, 5 on extra large screens -->
      <div class="grid grid-cols-1 sm:grid-cols-2 md:grid-cols-3 lg:grid-cols-4 xl:grid-cols-5 gap-4 sm:gap-6">
        <!-- Card Items -->
        <div v-for="item in cards" :key="item.title"
             class="p-4 bg-white rounded-lg shadow-md border border-gray-200 transition duration-300 ease-in-out hover:shadow-lg hover:border-gray-300">
          <h3 class="text-base font-bold text-gray-800">{{ item.title }}</h3>
          <p class="mt-1 text-sm text-gray-500">{{ item.description }}</p>
        </div>
      </div>
    </div>
  </div>
</template>

<style scoped>
/* TailwindCSS handles all styling */
</style>
