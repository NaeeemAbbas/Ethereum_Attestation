<script setup>
</script>

<template>
  <footer class="bg-[#001b3a] text-white py-10">
    <div class="max-w-7xl mx-auto grid grid-cols-1 md:grid-cols-4 gap-8 px-6">
      <!-- Logo and Description Section -->
      <div>
        <div class="flex items-center space-x-2">
          <!-- Logo Icon -->
          <svg xmlns="http://www.w3.org/2000/svg" class="h-8 w-8 text-blue-500" viewBox="0 0 24 24" fill="currentColor">
            <path d="M12 0L24 22H0z" />
          </svg>
          <!-- Logo Text -->
          <span class="text-2xl font-semibold">EAS</span>
        </div>
        <p class="mt-4 text-sm leading-relaxed">
          Ethereum Attestation Service is the global base layer for attestations.
        </p>
        <ul class="mt-4 space-y-1 text-sm">
          <li>Public good.</li>
          <li>Open Source.</li>
          <li>Permissionless.</li>
          <li>Tokenless.</li>
          <li>Free.</li>
        </ul>
      </div>

      <!-- Resources Section -->
      <div>
        <h3 class="text-lg font-semibold mb-4">Resources</h3>
        <ul class="space-y-2 text-sm">
          <li><a href="#" class="hover:underline">Explorer</a></li>
          <li><a href="#" class="hover:underline">Docs</a></li>
          <li><a href="#" class="hover:underline">FAQs</a></li>
        </ul>
      </div>

      <!-- Community Section -->
      <div>
        <h3 class="text-lg font-semibold mb-4">Community</h3>
        <ul class="space-y-2 text-sm">
          <li><a href="#" class="hover:underline">GitHub</a></li>
          <li><a href="#" class="hover:underline">Twitter</a></li>
        </ul>
      </div>

      <!-- General Section -->
      <div>
        <h3 class="text-lg font-semibold mb-4">General</h3>
        <ul class="space-y-2 text-sm">
          <li><a href="#" class="hover:underline">Why We Exist</a></li>
          <li><a href="#" class="hover:underline">The Vision</a></li>
          <li><a href="#" class="hover:underline">Core Concepts</a></li>
          <li><a href="#" class="hover:underline">Use Cases</a></li>
        </ul>
      </div>
    </div>
  </footer>
</template>
