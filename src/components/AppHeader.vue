<script setup>
import logo2 from '../assets/logo2.png'
import { ref } from "vue";
// Import the specific Lucide icons you need for this component
// Ensure you are importing from 'lucide-vue-next' for Vue 3 projects
import { Twitter, Github, MessageCircle, Menu, X } from 'lucide-vue-next'; // Added Menu and X icons

// Using ref for reactive data like active tab
const activeTab = ref("About");
const isMenuOpen = ref(false); // New reactive state for mobile menu visibility

const navLinks = [
  { name: "About", isActive: true }, // Set true for 'About' as it's active in the image
  { name: "Learn", isActive: false },
  { name: "Build", isActive: false },
  { name: "Explore", isActive: false },
  { name: "Engage", isActive: false },
];

const toggleMenu = () => {
  isMenuOpen.value = !isMenuOpen.value;
};

const selectTab = (tabName) => {
  activeTab.value = tabName;
  isMenuOpen.value = false; // Close menu when a tab is selected
};
</script>

<template>
  <header class="container mx-auto px-4 py-6 flex justify-between items-center relative">
    <div class="flex items-center space-x-2">
      <span class="font-bold font-serif text-2xl flex items-center cursor-pointer "> <img :src="logo2" class="h-8" alt="">EAS</span>
    </div>

    <nav class="hidden md:flex space-x-8 text-lg font-medium">
      <a
        v-for="link in navLinks"
        :key="link.name"
        :href="link.link || '#'"
        class="text-gray-800 hover:text-blue-600 border-b-2 border-transparent pb-1 -mb-1 transition-colors duration-200"
        :class="{ 'border-blue-600 text-blue-600': activeTab === link.name }"
        @click.prevent="activeTab = link.name"
      >
        {{ link.name }}
      </a>
    </nav>

    <div class="flex items-center space-x-4">
      <a href="#" class="text-gray-600 hover:text-blue-600">
        <Twitter class="h-6 w-6" />
      </a>
      <a href="#" class="text-gray-600 hover:text-blue-600">
        <Github class="h-6 w-6" />
      </a>
      <a href="#" class="text-gray-600 hover:text-blue-600">
        <MessageCircle class="h-6 w-6" />
      </a>
    </div>

    <button @click="toggleMenu" class="md:hidden text-gray-600 hover:text-blue-600 ml-4">
      <Menu v-if="!isMenuOpen" class="h-6 w-6" />
      <X v-else class="h-6 w-6" />
    </button>

    <transition name="slide">
      <nav
        v-if="isMenuOpen"
        class="md:hidden absolute top-full left-0 w-full bg-white shadow-lg py-4 z-50"
      >
        <a
          v-for="link in navLinks"
          :key="link.name"
          :href="link.link || '#'"
          class="block px-4 py-2 text-gray-800 hover:bg-gray-100"
          :class="{ 'bg-blue-50 text-blue-600': activeTab === link.name }"
          @click.prevent="selectTab(link.name)"
        >
          {{ link.name }}
        </a>
      </nav>
    </transition>
  </header>
</template>

<style scoped>
/* Transition for the mobile menu slide effect */
.slide-enter-active, .slide-leave-active {
  transition: transform 0.3s ease-out;
}
.slide-enter-from, .slide-leave-to {
  transform: translateY(-100%);
}
.slide-enter-to, .slide-leave-from {
  transform: translateY(0);
}
</style>