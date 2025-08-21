<script setup>
import { ref } from 'vue';
</script>

<template>
  <div class="flex items-center justify-center min-h-screen  mx-auto p-4 max-w-6xl">
    <div class="flex flex-wrap justify-center  items-center space-x-8">
     
      <div class="text-left">
        <h2 class="text-xl font-bold text-gray-800">Onchain</h2>
        <ul class="mt-2 space-y-1 text-gray-600">
          <li>Reputation Systems</li>
          <li>Oracles</li>
          <li>Registries</li>
          <li>So much more</li>
        </ul>
      </div>
    
      <div class="relative">
        <video src="/src//assets/gif.mp4" loop autoplay class="w-150 h-auto"></video>
        <div class="absolute -bottom-4 left-1/2 transform -translate-x-1/2">
          <svg width="24" height="24" fill="blue" viewBox="0 0 24 24">
           
          </svg>
        </div>
      </div>
      <!-- Right Offchain Section -->
      <div class="text-right">
        <h2 class="text-xl font-bold text-gray-800">Offchain</h2>
        <ul class="mt-2 space-y-1 text-gray-600">
          <li>P2P Attestations</li>
          <li>Social Networks</li>
          <li>Digital Identity</li>
          <li>Anything</li>
        </ul>
      </div>
    </div>
  </div>
</template>

<style scoped>
/* Add any custom styles here if needed */
</style>