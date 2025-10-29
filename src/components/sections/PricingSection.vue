<template>
  <section class="pricing" id="pricing">
    <div class="container">
      <div class="section-header">
        <h2 class="section-title">Pricing</h2>
        <p class="section-subtitle">
          Flexible plans designed for every daycare.
        </p>
      </div>
      
      <div class="pricing-cards">
        <div class="pricing-card starter">
          <div class="card-header">
            <div class="card-icon">
              <svg width="40" height="40" viewBox="0 0 24 24" fill="currentColor">
                <path d="M12 2C6.48 2 2 6.48 2 12s4.48 10 10 10 10-4.48 10-10S17.52 2 12 2zm-2 15l-5-5 1.41-1.41L10 14.17l7.59-7.59L19 8l-9 9z"/>
              </svg>
            </div>
            <h3 class="card-title">Starter</h3>
            <div class="card-price">$15 <span>/ Per month</span></div>
          </div>
          
          <ul class="card-features">
            <li>✓ Attendance tracking</li>
            <li>✓ Parent messages</li>
            <li>✓ Basic reports</li>
            <li>✓ Cloud storage</li>
          </ul>
          
          <button class="card-button">Get Start</button>
        </div>
        
        <div class="pricing-card business">
          <div class="card-header">
            <div class="card-icon">
              <svg width="40" height="40" viewBox="0 0 24 24" fill="currentColor">
                <path d="M7 7h10v3l4-4-4-4v3H5v6h2V7zm10 10H7v-3l-4 4 4 4v-3h12v-6h-2v4z"/>
              </svg>
            </div>
            <h3 class="card-title">Business</h3>
            <div class="card-price">$75 <span>/ Per month</span></div>
          </div>
          
          <ul class="card-features">
            <li>✓ Automated billing</li>
            <li>✓ Detailed analytics</li>
            <li>✓ Unlimited staff/children</li>
            <li>✓ Room/timetable management</li>
          </ul>
          
          <button class="card-button">Get Start</button>
        </div>
        
        <div class="pricing-card premium">
          <div class="card-header">
            <div class="card-icon">
              <svg width="40" height="40" viewBox="0 0 24 24" fill="currentColor">
                <path d="M19 6h-2c0-2.76-2.24-5-5-5S7 3.24 7 6H5c-1.1 0-1.99.9-1.99 2L3 20c0 1.1.9 2 2 2h14c1.1 0 2-.9 2-2V8c0-1.1-.9-2-2-2zm-7-3c1.66 0 3 1.34 3 3H9c0-1.66 1.34-3 3-3zm0 10c-2.76 0-5-2.24-5-5h2c0 1.66 1.34 3 3 3s3-1.34 3-3h2c0 2.76-2.24 5-5 5z"/>
              </svg>
            </div>
            <h3 class="card-title">Premium</h3>
            <div class="card-price">$95 <span>/ Per month</span></div>
          </div>
          
          <ul class="card-features">
            <li>✓ Multiple center management</li>
            <li>✓ Custom branding</li>
            <li>✓ Integrations</li>
            <li>✓ 24/7 support</li>
          </ul>
          
          <button class="card-button">Get Start</button>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
</script>

<style scoped>
.pricing {
  padding: var(--section-padding);
  background: var(--white);
}

.section-header {
  text-align: center;
}

.section-title {
  font-size: var(--font-size-h2);
  font-weight: 800;
  color: var(--primary-dark-blue);
  margin-bottom: 16px;
}

.section-subtitle {
  font-size: 1.125rem;
  color: #64748b;
  max-width: 600px;
  margin: 0 auto;
  line-height: 1.6;
}

.pricing-cards {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 32px;
  margin-top: 60px;
}

.pricing-card {
  background: var(--gray-light);
  border-radius: 16px;
  padding: 40px 32px;
  text-align: center;
  transition: transform 0.3s ease;
  border: 2px solid transparent;
}

.pricing-card:hover {
  transform: translateY(-8px);
}

.pricing-card.starter {
  border-color: var(--accent-yellow);
}

.pricing-card.business {
  border-color: var(--primary-light-blue);
  background: linear-gradient(135deg, #e0e7ff 0%, #f0f4ff 100%);
}

.pricing-card.premium {
  border-color: var(--accent-green);
}

.card-header {
  margin-bottom: 32px;
}

.card-icon {
  width: 60px;
  height: 60px;
  margin: 0 auto 16px;
  background: var(--white);
  border-radius: 12px;
  display: flex;
  align-items: center;
  justify-content: center;
  color: var(--primary-light-blue);
}

.pricing-card.starter .card-icon {
  color: var(--accent-yellow);
}

.pricing-card.business .card-icon {
  color: var(--primary-light-blue);
}

.pricing-card.premium .card-icon {
  color: var(--accent-green);
}

.card-title {
  font-size: 1.5rem;
  font-weight: 700;
  color: var(--primary-dark-blue);
  margin-bottom: 16px;
}

.card-price {
  font-size: 2rem;
  font-weight: 800;
  color: var(--primary-dark-blue);
}

.card-price span {
  font-size: 1rem;
  font-weight: 500;
  color: var(--gray);
}

.card-features {
  list-style: none;
  text-align: left;
  margin-bottom: 32px;
}

.card-features li {
  padding: 12px 0;
  color: var(--gray-dark);
  font-size: 0.95rem;
}

.card-button {
  width: 100%;
  padding: 14px 32px;
  border: none;
  border-radius: 8px;
  font-size: 1rem;
  font-weight: 600;
  cursor: pointer;
  transition: all 0.3s ease;
}

.pricing-card.starter .card-button {
  background: var(--accent-yellow);
  color: var(--white);
}

.pricing-card.business .card-button {
  background: var(--primary-light-blue);
  color: var(--white);
}

.pricing-card.premium .card-button {
  background: var(--accent-green);
  color: var(--white);
}

.card-button:hover {
  transform: scale(1.05);
  box-shadow: 0 4px 12px rgba(0, 0, 0, 0.2);
}

@media (max-width: 1024px) {
  .pricing-cards {
    grid-template-columns: repeat(2, 1fr);
  }
  
  .pricing-card.premium {
    grid-column: 1 / -1;
  }
}

@media (max-width: 768px) {
  .pricing-cards {
    grid-template-columns: 1fr;
  }
}
</style>





