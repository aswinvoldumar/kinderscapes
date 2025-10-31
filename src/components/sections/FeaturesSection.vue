<template>
  <section class="features" id="features">
    <div class="container">
      <div class="features-content">
        <div class="features-text">
          <h2 class="section-title">Experience the Future of Kinder Scapes</h2>
          <p class="features-description">
            Transform your daycare operations with our comprehensive platform designed to simplify management, 
            enhance parent communication, and create a more joyful learning environment for every child.
          </p>
          
          <ul class="features-list">
            <li class="feature-list-item">
              <span class="check-icon">✓</span>
              <span>Smart Attendance Tracking</span>
            </li>
            <li class="feature-list-item">
              <span class="check-icon">✓</span>
              <span>Automated Billing & Invoicing</span>
            </li>
            <li class="feature-list-item">
              <span class="check-icon">✓</span>
              <span>Child Progress & Activity Reports</span>
            </li>
          </ul>
          
          <button class="btn-primary" @click="openModal">
            Get a demo
          </button>
        </div>
        
        <div class="features-image">
          <img src="/src/assets/child.png" alt="Children Learning" class="child-image">
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
.features {
  padding: var(--section-padding);
  background: var(--gray-light);
}

.features-content {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 60px;
  align-items: center;
}

.section-title {
  color: var(--primary-dark-blue);
}

.features-description {
  font-size: 1.125rem;
  color: var(--gray);
  line-height: 1.7;
  margin-bottom: 32px;
}

.features-list {
  list-style: none;
  margin-bottom: 40px;
  display: flex;
  flex-direction: column;
  gap: 20px;
}

.feature-list-item {
  display: flex;
  align-items: center;
  gap: 16px;
  font-size: 1.125rem;
  color: var(--gray-dark);
}

.check-icon {
  width: 32px;
  height: 32px;
  background: var(--primary-light-blue);
  color: var(--white);
  border-radius: 50%;
  display: flex;
  align-items: center;
  justify-content: center;
  font-weight: 700;
  flex-shrink: 0;
}

.features-image {
  position: relative;
  display: flex;
  justify-content: center;
  align-items: center;
}

.child-image {
  width: 100%;
  max-width: 500px;
  height: auto;
  border-radius: 16px;
  box-shadow: 0 20px 40px rgba(0, 0, 0, 0.1);
  object-fit: cover;
}

@media (max-width: 1024px) {
  .features-content {
    grid-template-columns: 1fr;
  }
  
  .features-text {
    order: 1;
  }
  
  .features-image {
    order: 2;
  }
}

@media (max-width: 768px) {
  .section-title {
    font-size: 1.75rem;
  }
  
  .features-description {
    font-size: 1rem;
  }
  
  .child-image {
    max-width: 100%;
  }
}
</style>


