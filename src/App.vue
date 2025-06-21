<script setup>
import AppHeader from "./components/AppHeader.vue";
import Cards from "./components/Cards.vue";


import ContactUs from "./components/ContactUs.vue";
import ContractSection from "./components/ContractSection.vue";
import Faqs from "./components/Faqs.vue";
import FeaturesCard from "./components/featuresCard.vue";
import HeroSection from "./components/HeroSection.vue";
import Opportunities from "./components/Opportunities.vue";
import Scanner from "./components/Scanner.vue";
import Stack from "./components/Stack.vue";
import SubNavigation from "./components/SubNavigation.vue";
import Community from '@/components/Community.vue'
import Footer from '@/components/Footer.vue'
</script>

<template>
  <div class="font-sans antialiased text-gray-800">
    <div class="bg-purple-100 text-purple-800 py-2 text-center text-sm">
      Learn more about EAS in our docs
    </div>

    <AppHeader />

    <HeroSection />

    <SubNavigation />
    <FeaturesCard />
    <Faqs />
    <ContractSection/>
    <Scanner/>
    <Stack/>
    <Cards/>
    <Opportunities/>
    <ContactUs/>
    <Community/>
    <Footer/>
  </div>
</template>

<style scoped>
/* No specific scoped styles needed here, as Tailwind handles most of it
   and child components will have their own scoped styles. */
</style>
