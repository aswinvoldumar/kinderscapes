<template>
  <section class="poster-model">
    <div class="container">
      <div class="poster-content">
        <!-- Left Marketing Panel -->
        <div class="marketing-panel">
          <h2 class="marketing-title">The best day care<br>management in<br>your fingertips.</h2>
          <p class="marketing-subtitle">Made with love to make every daycare day<br>easier.</p>
          <button class="cta-button" @click="openModal">
            Start free 14 trial
            <svg width="16" height="16" fill="none" stroke="currentColor" viewBox="0 0 24 24">
              <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M9 5l7 7-7 7"/>
            </svg>
          </button>
        </div>
        
        <!-- Right Dashboard Image -->
        <div class="dashboard-panel">
          <img src="/src/assets/message.png" alt="Dashboard Preview" class="dashboard-image">
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
import { inject } from 'vue'

const openModal = inject('openModal')
</script>

<style scoped>
.poster-model {
  padding: var(--section-padding);
  background-size: cover;
  background-position: center;
  background-repeat: no-repeat;
  color: var(--white);
  min-height: 600px;
}

.poster-content {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 0;
  align-items: center;
  height: 100%;
  max-width: 1200px;
  margin: 0 auto;
}

.marketing-panel {
  background: var(--primary-blue);
  padding: 80px 60px;
  border-radius: 24px 0 0 24px;
  height: 500px;
  display: flex;
  flex-direction: column;
  justify-content: center;
}

.dashboard-panel {
  height: 500px;
  display: flex;
  align-items: flex-start;
  justify-content: flex-start;
  background: var(--primary-blue);
  border-radius: 0 24px 24px 0;
  overflow: hidden;
  padding: 20px 0 0 20px;
}

.dashboard-image {
  width: calc(100% - 20px);
  height: calc(100% - 20px);
  object-fit: cover;
  border-radius: 0 24px 24px 0;
}

.marketing-title {
  font-size: 3rem;
  font-weight: 800;
  color: var(--white);
  margin-bottom: 24px;
  line-height: 1.2;
  text-align: left;
}

.marketing-subtitle {
  font-size: 1.25rem;
  color: var(--white);
  opacity: 0.9;
  margin-bottom: 40px;
  text-align: left;
  line-height: 1.4;
}

.cta-button {
  background: var(--white);
  color: var(--primary-blue);
  padding: 16px 32px;
  border: none;
  border-radius: 8px;
  font-size: 1rem;
  font-weight: 600;
  cursor: pointer;
  transition: all 0.3s ease;
  display: inline-flex;
  align-items: center;
  gap: 8px;
  align-self: flex-start;
}

.cta-button:hover {
  transform: translateY(-2px);
  box-shadow: 0 8px 24px rgba(255, 255, 255, 0.2);
}


@media (max-width: 1024px) {
  .poster-content {
    grid-template-columns: 1fr;
    gap: 0;
  }
  
  .marketing-panel {
    border-radius: 24px 24px 0 0;
    order: 1;
  }
  
  .dashboard-panel {
    border-radius: 0 0 24px 24px;
    order: 2;
  }
  
  .dashboard-image {
    border-radius: 0 0 24px 24px;
  }
}

@media (max-width: 768px) {
  .marketing-panel {
    padding: 60px 40px;
    height: 400px;
  }
  
  .dashboard-panel {
    height: 300px;
  }
  
  .marketing-title {
    font-size: 2.5rem;
  }
  
  .marketing-subtitle {
    font-size: 1.125rem;
  }
}

@media (max-width: 480px) {
  .marketing-panel {
    padding: 40px 24px;
    height: 350px;
  }
  
  .dashboard-panel {
    height: 250px;
  }
  
  .marketing-title {
    font-size: 2rem;
  }
  
  .marketing-subtitle {
    font-size: 1rem;
  }
  
  .cta-button {
    padding: 12px 24px;
    font-size: 0.9rem;
  }
}
</style>


