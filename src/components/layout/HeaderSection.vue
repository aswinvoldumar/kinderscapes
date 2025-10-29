<template>
  <header class="header" :class="{ 'scrolled': isScrolled }">
    <div class="container">
      <div class="header-content">
        <div class="logo">
          <img src="/src/assets/kinder logo.png" alt="Kinder Scapes Logo" class="logo-image" />
          <div class="logo-text">
            <div class="logo-title">KINDER SCAPES</div>
            <div class="logo-tagline">DAYCARE MANAGEMENT SOFTWARE</div>
          </div>
        </div>
        
        <nav class="nav">
          <a href="#home" 
             class="nav-link" 
             :class="{ active: activeLink === 'home' }"
             @click.prevent="setActiveLink('home'); scrollToSection('home')">Home</a>
          <a href="#features" 
             class="nav-link" 
             :class="{ active: activeLink === 'features' }"
             @click.prevent="setActiveLink('features'); scrollToSection('features')">Features</a>
          <a href="#how-it-works" 
             class="nav-link" 
             :class="{ active: activeLink === 'how-it-works' }"
             @click.prevent="setActiveLink('how-it-works'); scrollToSection('how-it-works')">How does it work</a>
          <a href="#pricing" 
             class="nav-link" 
             :class="{ active: activeLink === 'pricing' }"
             @click.prevent="setActiveLink('pricing'); scrollToSection('pricing')">Pricing</a>
          <a href="#reviews" 
             class="nav-link" 
             :class="{ active: activeLink === 'reviews' }"
             @click.prevent="setActiveLink('reviews'); scrollToSection('reviews')">Reviews</a>
        </nav>
        
        <button class="cta-button">
          Start free 14 trial
          <svg width="16" height="16" fill="none" stroke="currentColor" viewBox="0 0 24 24">
            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M9 5l7 7-7 7"/>
          </svg>
        </button>
      </div>
    </div>
  </header>
</template>

<script setup>
import { ref, onMounted, onUnmounted } from 'vue'

const isScrolled = ref(false)
const activeLink = ref('home')

const handleScroll = () => {
  isScrolled.value = window.scrollY > 50
}

const setActiveLink = (link) => {
  activeLink.value = link
}

const scrollToSection = (sectionId) => {
  const element = document.getElementById(sectionId)
  if (element) {
    element.scrollIntoView({ 
      behavior: 'smooth',
      block: 'start'
    })
  }
}

onMounted(() => {
  window.addEventListener('scroll', handleScroll)
})

onUnmounted(() => {
  window.removeEventListener('scroll', handleScroll)
})
</script>

<style scoped>
.header {
  position: fixed;
  top: 0;
  left: 0;
  right: 0;
  background: transparent;
  box-shadow: none;
  z-index: 1000;
  transition: all 0.3s ease;
}

.header.scrolled {
  background: var(--primary-blue);
  box-shadow: 0 2px 20px rgba(0, 0, 0, 0.15);
}

.header-content {
  display: flex;
  align-items: center;
  justify-content: space-between;
  padding: 1.5rem 0;
  min-height: 80px;
  width: 100%;
}

.header-content .logo {
  flex: 0 0 auto;
  order: 1;
  margin-right: auto;
}

.header-content .nav {
  flex: 0 0 auto;
  order: 2;
  display: flex;
  gap: 10px;
  align-items: center;
  margin-left: auto;
  margin-right: 2rem;
}

.header-content .cta-button {
  flex: 0 0 auto;
  order: 3;
  margin-left: 0;
}

.logo {
  display: flex;
  align-items: center;
  gap: 16px;
}

.logo-image {
  width: 60px;
  height: 60px;
  object-fit: contain;
}

.logo-text {
  display: flex;
  flex-direction: column;
  gap: 2px;
}

.logo-title {
  font-size: 1.5rem;
  font-weight: 700;
  color: var(--white);
  line-height: 1.2;
  letter-spacing: 0.5px;
}

.logo-tagline {
  font-size: 0.75rem;
  font-weight: 400;
  color: rgba(255, 255, 255, 0.8);
  line-height: 1.2;
  letter-spacing: 0.3px;
}


.nav-link {
  text-decoration: none;
  color: var(--white);
  font-size: 1rem;
  font-weight: 500;
  transition: all 0.3s ease;
  position: relative;
  padding: 12px 16px;
  border-radius: 8px;
  background: transparent;
}

.nav-link:hover {
  color: var(--white);
  background: rgba(255, 255, 255, 0.1);
  transform: translateY(-2px);
  box-shadow: 0 4px 12px rgba(255, 255, 255, 0.1);
}

.nav-link.active {
  font-weight: 600;
  color: var(--white);
  background: rgba(255, 255, 255, 0.15);
  box-shadow: 0 4px 12px rgba(255, 255, 255, 0.2);
}

.nav-link.active::after {
  content: '';
  position: absolute;
  bottom: 4px;
  left: 50%;
  transform: translateX(-50%);
  width: 6px;
  height: 6px;
  background-color: var(--white);
  border-radius: 50%;
  box-shadow: 0 0 8px rgba(255, 255, 255, 0.5);
}

.cta-button {
  background-color: var(--white);
  color: var(--primary-dark-blue);
  padding: 12px 24px;
  border: none;
  border-radius: 8px;
  font-size: 0.95rem;
  font-weight: 600;
  cursor: pointer;
  transition: all 0.3s ease;
  display: inline-flex;
  align-items: center;
  gap: 8px;
  box-shadow: 0 2px 8px rgba(0, 0, 0, 0.1);
}

.cta-button:hover {
  background-color: rgba(255, 255, 255, 0.95);
  transform: translateY(-2px);
  box-shadow: 0 4px 12px rgba(0, 0, 0, 0.15);
}

@media (max-width: 1024px) {
  .header-content .nav {
    gap: 24px;
  }
  
  .nav-link {
    font-size: 0.9rem;
  }
}

@media (max-width: 768px) {
  .header-content {
    padding: 1rem 0;
    min-height: 70px;
  }
  
  .logo {
    gap: 12px;
  }
  
  .logo-image {
    width: 50px;
    height: 50px;
  }
  
  .logo-title {
    font-size: 1.25rem;
  }
  
  .logo-tagline {
    font-size: 0.7rem;
  }
  
  .header-content .nav {
    display: none;
  }
  
  .cta-button {
    padding: 10px 20px;
    font-size: 0.875rem;
  }
}

@media (max-width: 480px) {
  .logo {
    gap: 10px;
  }
  
  .logo-image {
    width: 45px;
    height: 45px;
  }
  
  .logo-title {
    font-size: 1.1rem;
  }
  
  .logo-tagline {
    font-size: 0.65rem;
  }
  
  .cta-button {
    padding: 8px 16px;
    font-size: 0.8rem;
  }
}
</style>

