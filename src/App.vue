<script setup>
import { ref, provide } from 'vue'
import HeaderSection from './components/layout/HeaderSection.vue'
import HeroSection from './components/sections/HeroSection.vue'
import TrustedBySection from './components/sections/TrustedBySection.vue'
import HowItWorksSection from './components/sections/HowItWorksSection.vue'
import AnalyzeDataSection from './components/sections/AnalyzeDataSection.vue'
import UsersSection from './components/sections/UsersSection.vue'
import PricingSection from './components/sections/PricingSection.vue'
import FeaturesSection from './components/sections/FeaturesSection.vue'
import TestimonialsSection from './components/sections/TestimonialsSection.vue'
import PosterModelSection from './components/sections/PosterModelSection.vue'
import FooterSection from './components/layout/FooterSection.vue'
import FreeTrialModal from './components/FreeTrialModal.vue'

const showModal = ref(false)

const openModal = () => {
  showModal.value = true
}

const closeModal = () => {
  showModal.value = false
}

// Provide the openModal function to all child components
provide('openModal', openModal)
</script>

<template>
  <div id="app">
    <HeaderSection />
    <section id="home">
      <HeroSection />
    </section>
    <!-- <TrustedBySection /> -->
    <br>
    <section id="how-it-works">
      <HowItWorksSection />
    </section>
    <AnalyzeDataSection />
    <section id="pricing">
      <PricingSection />
      <UsersSection/>
    </section>
    <section id="features">
      <FeaturesSection />
    </section>
    <section id="reviews">
      <!-- <TestimonialsSection /> -->
    </section>
    <PosterModelSection />
    <FooterSection />
    <FreeTrialModal :isVisible="showModal" @close="closeModal" />
  </div>
</template>

<style>
#app {
  width: 100%;
  margin: 0;
  padding: 0;
  font-family: 'Inter', -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, sans-serif;
}
</style>
