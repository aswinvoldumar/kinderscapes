<template>
  <section class="trusted-by">
    <!-- <div class="container">
      <div class="trusted-by-content">
        <div class="logo-item">LOGO IPSUM</div>
        <div class="logo-item">
          <svg width="24" height="24" viewBox="0 0 24 24" fill="currentColor">
            <path d="M12 2L2 7l10 5 10-5-10-5zM2 17l10 5 10-5M2 12l10 5 10-5"/>
          </svg>
          LOGOIPSUM
        </div>
        <div class="logo-item">
          <svg width="24" height="24" viewBox="0 0 24 24" fill="currentColor">
            <path d="M12 2L2 7v10c0 5.55 3.84 10.74 9 12 5.16-1.26 9-6.45 9-12V7l-10-5z"/>
          </svg>
          LOGO IPSUM
        </div>
        <div class="logo-item">
          <svg width="24" height="24" viewBox="0 0 24 24" fill="currentColor">
            <circle cx="12" cy="12" r="10"/>
          </svg>
          LOGO IPSUM
        </div>
      </div>
    </div> -->
  </section>
</template>

<script setup>
</script>

<style scoped>
.trusted-by {
  margin-top: 200px;
  padding: 170px 20px 60px;
  background: var(--white);
}

.trusted-by-content {
  display: flex;
  justify-content: space-around;
  align-items: center;
  flex-wrap: wrap;
  gap: 40px;
}

.logo-item {
  display: flex;
  align-items: center;
  gap: 8px;
  font-size: 1.25rem;
  font-weight: 600;
  color: var(--gray);
  opacity: 0.7;
  transition: opacity 0.3s ease;
}

.logo-item:hover {
  opacity: 1;
}

@media (max-width: 768px) {
  .trusted-by-content {
    justify-content: center;
  }
  
  .logo-item {
    font-size: 1rem;
  }
}
</style>

