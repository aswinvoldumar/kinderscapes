<template>
  <section class="testimonials" id="reviews">
    <div class="container">
      <div class="section-header">
        <h2 class="section-title">Testimonial</h2>
        <p class="section-subtitle">
          Trusted by Educators & Families
        </p>
      </div>
      
      <div class="testimonials-grid">
        <div class="testimonial-card">
          <h3 class="testimonial-title">Reports and billing</h3>
          <p class="testimonial-quote">
            "Managing reports and billing has never been easier. The automation saves us hours every week, 
            and the real-time updates keep us organized."
          </p>
          <div class="testimonial-author">
            <div class="author-avatar">PN</div>
            <div class="author-info">
              <div class="author-name">Priya Nair</div>
              <div class="author-company">Little Steps Preschool</div>
            </div>
          </div>
        </div>
        
        <div class="testimonial-card">
          <h3 class="testimonial-title">Communication</h3>
          <p class="testimonial-quote">
            "The parent communication features are incredible. Daily updates, photos, and instant messaging 
            have completely transformed how we connect with families."
          </p>
          <div class="testimonial-author">
            <div class="author-avatar">RM</div>
            <div class="author-info">
              <div class="author-name">Rahul Mehta</div>
              <div class="author-company">Bright Minds Daycare</div>
            </div>
          </div>
        </div>
        
        <div class="testimonial-card">
          <h3 class="testimonial-title">Attendance, payments</h3>
          <p class="testimonial-quote">
            "Everything we need in one place - attendance, payments, and daily activities. It's streamlined 
            our entire operation and made our center more efficient."
          </p>
          <div class="testimonial-author">
            <div class="author-avatar">AG</div>
            <div class="author-info">
              <div class="author-name">Anita George</div>
              <div class="author-company">Tiny Hearts Daycare</div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
</script>

<style scoped>
.testimonials {
  padding: var(--section-padding);
  background: var(--white);
}

.testimonials-grid {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 32px;
  margin-top: 60px;
}

.testimonial-card {
  background: var(--gray-light);
  padding: 40px 32px;
  border-radius: 16px;
  transition: transform 0.3s ease, box-shadow 0.3s ease;
}

.testimonial-card:hover {
  transform: translateY(-8px);
  box-shadow: 0 10px 40px rgba(0, 0, 0, 0.1);
}

.testimonial-title {
  font-size: 1.25rem;
  font-weight: 700;
  color: var(--primary-dark-blue);
  margin-bottom: 16px;
}

.testimonial-quote {
  font-size: 1rem;
  color: var(--gray);
  line-height: 1.7;
  margin-bottom: 32px;
}

.testimonial-author {
  display: flex;
  align-items: center;
  gap: 16px;
}

.author-avatar {
  width: 56px;
  height: 56px;
  border-radius: 50%;
  background: var(--primary-light-blue);
  color: var(--white);
  display: flex;
  align-items: center;
  justify-content: center;
  font-size: 1.25rem;
  font-weight: 700;
  flex-shrink: 0;
}

.author-info {
  flex: 1;
}

.author-name {
  font-size: 1rem;
  font-weight: 600;
  color: var(--primary-dark-blue);
  margin-bottom: 4px;
}

.author-company {
  font-size: 0.875rem;
  color: var(--gray);
}

@media (max-width: 1024px) {
  .testimonials-grid {
    grid-template-columns: repeat(2, 1fr);
  }
  
  .testimonial-card:last-child {
    grid-column: 1 / -1;
  }
}

@media (max-width: 768px) {
  .testimonials-grid {
    grid-template-columns: 1fr;
  }
}
</style>







