<script setup>
// No script logic required for this static layout
</script>

<template>
  <div class="p-4 sm:p-8 bg-gray-50 rounded-xl shadow-lg max-w-6xl mx-auto space-y-6 sm:space-y-8">
    <!-- Badge -->
    <div class="flex justify-center">
      <span class="px-4 py-2 text-sm font-semibold text-blue-600 bg-blue-100 rounded-full">
        Built for Everyone
      </span>
    </div>

    <!-- Title and Description -->
    <div class="text-center">
      <h1 class="text-2xl sm:text-3xl lg:text-4xl font-bold text-gray-800 leading-tight">
        Public Good. Open-Source. Permissionless. Token-Free.
      </h1>
      <p class="mt-2 text-base sm:text-lg text-gray-500 max-w-2xl mx-auto">
        Easily start building with others on mainnet, leading L2s, and various testnets.
      </p>
    </div>

    <!-- Grid of Cards -->
    <!--
      This section uses a responsive grid layout.
      - On small screens (default), it's a 2-column grid.
      - On medium screens (md), it becomes a 3-column grid.
      - On large screens (lg), it shifts to a 4-column grid.
      - On extra-large screens (xl), it displays all 7 items in a single row.
      'gap-4' provides spacing between the grid items.
    -->
    <div class="grid grid-cols-2 md:grid-cols-3 lg:grid-cols-4 xl:grid-cols-7 gap-4">
      <div class="flex items-center justify-center w-full h-16 bg-white rounded-lg border border-gray-200 shadow-sm transition duration-300 ease-in-out hover:shadow-md hover:border-gray-300 cursor-pointer">
        <span class="font-bold text-gray-700">OPTIMISM</span>
      </div>
      <div class="flex items-center justify-center w-full h-16 bg-white rounded-lg border border-gray-200 shadow-sm transition duration-300 ease-in-out hover:shadow-md hover:border-gray-300 cursor-pointer">
        <span class="font-bold text-gray-700">coinbase</span>
      </div>
      <div class="flex items-center justify-center w-full h-16 bg-white rounded-lg border border-gray-200 shadow-sm transition duration-300 ease-in-out hover:shadow-md hover:border-gray-300 cursor-pointer">
        <span class="font-bold text-gray-700">GITCOIN</span>
      </div>
      <div class="flex items-center justify-center w-full h-16 bg-white rounded-lg border border-gray-200 shadow-sm transition duration-300 ease-in-out hover:shadow-md hover:border-gray-300 cursor-pointer">
        <span class="font-bold text-gray-700">ARBITRUM</span>
      </div>
      <div class="flex items-center justify-center w-full h-16 bg-white rounded-lg border border-gray-200 shadow-sm transition duration-300 ease-in-out hover:shadow-md hover:border-gray-300 cursor-pointer">
        <span class="font-bold text-gray-700">Devfolio</span>
      </div>
      <div class="flex items-center justify-center w-full h-16 bg-white rounded-lg border border-gray-200 shadow-sm transition duration-300 ease-in-out hover:shadow-md hover:border-gray-300 cursor-pointer">
        <span class="font-bold text-gray-700">ceramic</span>
      </div>
      <div class="flex items-center justify-center w-full h-16 bg-white rounded-lg border border-gray-200 shadow-sm transition duration-300 ease-in-out hover:shadow-md hover:border-gray-300 cursor-pointer">
        <span class="font-bold text-gray-700">ETHGlobal</span>
      </div>
    </div>

    <!-- Stats Section -->
    <!--
      This section also uses a responsive flex layout.
      - On small screens (default), items stack vertically (flex-col).
      - On medium screens (md), items are arranged horizontally (flex-row).
      'gap-y-6' for vertical spacing on small screens, 'md:gap-x-12' for horizontal spacing on medium and larger.
      The 'EAS is growing' text is now properly part of the flex container.
    -->
    <div class="flex flex-col md:flex-row items-center justify-around gap-y-6 md:gap-y-0 md:gap-x-12 text-center py-4">
      <div class="flex-shrink-0">
        <span class="font-bold text-gray-800 text-2xl sm:text-3xl">EAS is growing</span>
      </div>
      <div>
        <span class="text-4xl font-bold text-gray-800">7M+</span>
        <p class="text-sm text-gray-500">attestations made</p>
      </div>
      <div>
        <span class="text-4xl font-bold text-gray-800">420k+</span>
        <p class="text-sm text-gray-500">unique attesters</p>
      </div>
      <div>
        <span class="text-4xl font-bold text-gray-800">1.4M+</span>
        <p class="text-sm text-gray-500">recipients</p>
      </div>
    </div>

    <!-- Call-to-Action Button -->
    <div class="flex justify-center pt-4">
      <button class="px-8 py-3 my-2 text-base cursor-pointer font-medium text-black border border-gray-300 rounded-lg shadow hover:bg-black hover:text-white transition duration-300 ease-in-out">
        Explore the Ecosystem
      </button>
    </div>
  </div>
</template>

<style scoped>
/* TailwindCSS handles all styling */
</style>
