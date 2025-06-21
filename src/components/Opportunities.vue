<script setup>
import { ref } from 'vue';

const useCases = ref([
  {
    title: 'Identity',
    description: 'Aggregate attested and offchain identities.',
  },
  {
    title: 'Ticketing',
    description: 'Issue and verify tickets to events.',
  },
  {
    title: 'Trust Networks',
    description: 'Reputation systems & trust scores onchain.',
  },
  {
    title: 'Social Networks',
    description: 'Verified and user controlled social networks.',
  },
  {
    title: 'Voting Systems',
    description: 'Voting for local, national, & global communities.',
  },
  {
    title: 'Oracles',
    description: 'Attest to real world outcomes and offchain information.',
  },
  {
    title: 'Undercollateralized Loans',
    description: 'Credit scores and financial status.',
  },
  {
    title: 'Agent Interactions',
    description: 'Reputations, attested data, authorizations.',
  },
  {
    title: 'Signing documents',
    description: 'Digital notary and signing services.',
  },
  {
    title: 'Proof of provenance',
    description: 'Know the origination of the goods you buy.',
  },
]);
</script>

<template>
  <div class="bg-gradient-to-b from-blue-50 to-orange-50 py-16 sm:py-24 px-4 sm:px-6 lg:px-8">
    <div class="max-w-7xl mx-auto">
      <div class="text-center mb-12 sm:mb-16">
        <h2 class="text-4xl sm:text-5xl font-extrabold text-gray-900 leading-tight mb-4">
          What will you build?
        </h2>
        <p class="text-base sm:text-lg text-gray-600 max-w-xl mx-auto">
          Get inspired. The opportunities the attestation layer creates are endless.
        </p>
      </div>

      <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-2 xl:grid-cols-2 gap-6 sm:gap-8 max-w-4xl mx-auto">
        <div v-for="(useCase, index) in useCases" :key="index"
             class="bg-white rounded-lg shadow-sm border border-gray-200 p-6 text-center
                    transition-all duration-300 ease-in-out hover:shadow-md hover:border-blue-300">
          <h3 class="text-xl font-semibold text-gray-800 mb-2">
            {{ useCase.title }}
          </h3>
          <p class="text-gray-600 text-sm">
            {{ useCase.description }}
          </p>
        </div>
      </div>

      <div class="text-center mt-12 sm:mt-16">
        <button class="inline-flex items-center px-6 py-3 border border-gray-300 shadow-sm cursor-pointer
                       text-base font-medium rounded-md text-gray-700 bg-white
                       hover:bg-black hover:text-white focus:outline-none focus:ring-2
                       focus:ring-offset-2 focus:ring-blue-500 transition-colors duration-200">
          Use Case Examples
        </button>
      </div>
    </div>
  </div>
</template>

<style scoped>
/* No specific scoped styles are needed as Tailwind CSS handles everything */
</style>