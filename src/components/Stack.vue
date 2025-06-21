<script setup></script>

<template>
  <div class="bg-white py-12 sm:py-16 px-4 sm:px-6 lg:px-8">
    <div class="max-w-7xl mx-auto">
      <!-- Title and Description Section -->
      <div class="text-center mb-12">
        <h1 class="text-4xl sm:text-5xl lg:text-6xl font-bold text-gray-900 leading-tight mb-4">
          EAS is the base layer.
        </h1>
        <p class="text-base sm:text-lg text-gray-700 max-w-3xl mx-auto">
          EAS is designed to be that foundational infrastructure for the attestation
          ecosystem. Neutral, open, and built for the community, without
          presupposing too much or building too high in the stack.
        </p>
      </div>

      <!-- Pyramid Diagram Section -->
      <div class="flex flex-col items-center    ">

        <!-- Layer 1: Impact -->
        <div class="w-full max-w-xl p-4 bg-white border border-gray-300 rounded-lg shadow-md text-center">
          <h3 class="font-bold text-lg text-gray-800">Impact</h3>
          <p class="text-sm text-gray-600 mt-1">Attestations build trust online + onchain.</p>
        </div>

        <!-- Layer 2: Application Layer -->
        <div class="w-full max-w-2xl p-4 bg-white border border-gray-300 rounded-lg shadow-md text-center">
          <h3 class="font-bold text-lg text-gray-800">Application Layer</h3>
          <p class="text-sm text-gray-600 mt-1">New and existing apps become more trustful and composable</p>
          <div class="flex flex-wrap justify-center gap-x-6 gap-y-2 mt-3 text-sm font-medium text-gray-700">
            <span>Reputation Graphs</span>
            <span>Digital Identity</span>
            <span>Provenance & Proofs</span>
            <span>Voting Systems</span>
            <span>Ticketing</span>
            <span>Moral</span>
          </div>
        </div>

        <!-- Layer 3: Attestation Layer -->
        <div class="w-full max-w-3xl p-4 bg-white border border-gray-300 rounded-lg shadow-md text-center">
          <h3 class="font-bold text-lg text-gray-800">Attestation Layer</h3>
          <p class="text-sm text-gray-600 mt-1">Where any type of entity makes attestations about anything.</p>
          <div class="flex flex-wrap justify-center gap-x-6 gap-y-2 mt-3 text-sm font-medium text-gray-700">
            <span>Peer to Peer</span>
            <span>Organizations</span>
            <span>Contract to Contract</span>
            <span>Governments</span>
            <span>Machine to Machine</span>
            <span>Communities</span>
          </div>
        </div>

        <!-- Layer 4: Ethereum Attestation Service (The Base) -->
        <div class="w-full max-w-4xl p-6 bg-[#98AEEB] border border-blue-700 rounded-lg shadow-lg text-center text-white">
          <h3 class="font-bold text-xl sm:text-2xl">Ethereum Attestation Service</h3>
          <p class="text-sm sm:text-base mt-2">
            The universal and community-led base layer where schemas are registered and attestations are made.
          </p>
        </div>

        <!-- Layer 5: Settlement Layer -->
        <div class="w-full max-w-5xl p-4 bg-white border border-gray-300 rounded-lg shadow-md text-center">
          <h3 class="font-bold text-lg text-gray-800">Settlement Layer</h3>
          <p class="text-sm text-gray-600 mt-1">Where attestations are settled and can be verified onchain or offchain.</p>
          <div class="flex flex-wrap justify-center gap-x-6 gap-y-2 mt-3 text-sm font-medium text-gray-700">
            <span>Ethereum</span>
            <span>Layer 2s</span>
            <span>Offchain</span>
          </div>
        </div>

      </div>
    </div>
  </div>
</template>

<style scoped>
/* No specific scoped styles are needed as Tailwind CSS handles everything */
</style>
