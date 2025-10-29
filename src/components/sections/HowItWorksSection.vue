<template>
  <section class="how-it-works" id="how-it-works">
    <div class="container">
      <div class="section-header">
        <h2 class="section-title">How Does it Work?</h2>
        <p class="section-subtitle">
          Using basic skills you can improve your business stuff with Around
        </p>
      </div>
      
      <div class="steps-grid">
        <div class="step-card">
          <div class="step-number">1</div>
          <h3 class="step-title">Register Your Center</h3>
          <p class="step-description">
            Create your account, add your staff, and set up classrooms within minutes.
          </p>
        </div>
        
        <div class="step-card">
          <div class="step-number">2</div>
          <h3 class="step-title">Manage Daily Operations</h3>
          <p class="step-description">
            Track attendance, send messages, manage billing, and monitor reports — all from one dashboard.
          </p>
        </div>
        
        <div class="step-card">
          <div class="step-number">3</div>
          <h3 class="step-title">Connect with Parents</h3>
          <p class="step-description">
            Share real-time updates, daily reports, and announcements through the parent portal or app.
          </p>
        </div>
        
        <div class="step-card">
          <div class="step-number">4</div>
          <h3 class="step-title">Access to Dashboard from all devices</h3>
          <p class="step-description">
            Using basic skills you can improve your business stuff with Around using basic tools.
          </p>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
</script>

<style scoped>
.how-it-works {
  padding: var(--section-padding);
  background: var(--gray-light);
}

.section-header {
  text-align: center;
  margin-bottom: 60px;
}

.section-title {
  font-size: var(--font-size-h2);
  font-weight: 800;
  color: var(--primary-dark-blue);
  margin-bottom: 16px;
}

.section-subtitle {
  font-size: 1.125rem;
  color: var(--gray);
  max-width: 600px;
  margin: 0 auto;
}

.steps-grid {
  display: grid;
  grid-template-columns: repeat(2, 1fr);
  gap: 32px;
}

.step-card {
  background: var(--primary-light-blue);
  color: var(--white);
  padding: 48px 32px;
  border-radius: 16px;
  transition: transform 0.3s ease;
}

.step-card:hover {
  transform: translateY(-8px);
}

.step-number {
  font-size: 3rem;
  font-weight: 900;
  opacity: 0.3;
  margin-bottom: 16px;
}

.step-title {
  font-size: 1.5rem;
  font-weight: 700;
  margin-bottom: 16px;
}

.step-description {
  font-size: 1rem;
  opacity: 0.95;
  line-height: 1.6;
}

@media (max-width: 768px) {
  .steps-grid {
    grid-template-columns: 1fr;
  }
  
  .step-card {
    padding: 32px 24px;
  }
}
</style>

