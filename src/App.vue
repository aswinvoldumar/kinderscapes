<script setup>
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
</script>

<template>
  <div id="app">
    <HeaderSection />
    <section id="home">
      <HeroSection />
    </section>
    <TrustedBySection />
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
      <TestimonialsSection />
    </section>
    <PosterModelSection />
    <FooterSection />
    
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
