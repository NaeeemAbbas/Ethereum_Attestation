<script setup>
import { Github } from 'lucide-vue-next';

// No specific reactive data needed for this static content component
</script>

<template>
  <section class="relative pt-24 pb-32 text-center overflow-hidden">
    <div
      class="absolute inset-0 z-0 opacity-50"
      style="background: linear-gradient(to bottom, #eff6ff, #dbeafe)"
    ></div>

    <div class="relative z-10 container mx-auto px-4">
      <h1
        class=" md:text-7xl lg:text-6xl  font-extrabold leading-tight tracking-tight mb-8"
      >
        Attest to anything<br />and everything.
      </h1>
      <p class="text-xl md:text-xl text-gray-600 max-w-2xl mx-auto mb-12">
        <span class="font-semibold">Ethereum Attestation Service (EAS)</span> is an
        infrastructure public good for making attestations onchain or offchain about
        anything.
      </p>
      <div
        class="flex flex-col sm:flex-row justify-center space-y-4 sm:space-y-0 sm:space-x-6"
      >
        <button
          class="cursor-pointer flex items-center justify-center px-8 py-4 bg-white border border-gray-300 rounded-lg shadow-sm text-lg font-medium text-gray-900 hover:bg-gray-50 transition-colors duration-200"
        >
          <Github class="h-6 w-6 mr-3" />
          Welcome to EAS
        </button>
        <button
          class="cursor-pointer flex items-center justify-center px-8 py-4 bg-black text-white rounded-lg shadow-md text-lg font-medium hover:bg-gray-800 transition-colors duration-200"
        >
          Start Exploring
          <span class="ml-3 text-2xl">&rarr;</span>
        </button>
      </div>
    </div>
  </section>
</template>

<style scoped>
/* No specific scoped styles needed */
</style>
