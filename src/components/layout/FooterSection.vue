<template>
  <footer class="footer">
    <div class="container">
      <div class="footer-content">
        <div class="footer-column">
          <a href="#home" class="footer-logo" @click.prevent="scrollToHome">
            <img src="/src/assets/kinder logo.png" alt="Kinder Scapes Logo" class="footer-logo-image" />
            <div class="footer-logo-text">
              <div class="footer-logo-title">KINDER SCAPES</div>
              <div class="footer-logo-tagline">DAYCARE MANAGEMENT SOFTWARE</div>
            </div>
          </a>
          <p class="footer-description">
            Empowering educators and caregivers to create a warm & nurturing environment for children with less paperwork.
          </p>
        </div>
        
        <div class="footer-column">
          <h4 class="footer-heading">Explore</h4>
          <ul class="footer-links">
            <li><a href="#features">Feature</a></li>
            <li><a href="#who-to-use">How to use</a></li>
            <li><a href="#pricing">Pricing</a></li>
            <li><a href="#reviews">Reviews</a></li>
          </ul>
        </div>
        
        <div class="footer-column">
          <h4 class="footer-heading">Support</h4>
          <ul class="footer-links">
            <li><a href="#">Privacy policy</a></li>
            <li><a href="#">Legal</a></li>
            <li><a href="#">Terms of service</a></li>
            <li><a href="#">Help center</a></li>
          </ul>
        </div>
        
        <div class="footer-column">
          <h4 class="footer-heading">Follow Us</h4>
          <div class="social-icons">
            <a href="#" class="social-icon" target="_blank" rel="noopener noreferrer">
              <svg width="24" height="24" viewBox="0 0 24 24" fill="currentColor">
                <path d="M20.447 20.452h-3.554v-5.569c0-1.328-.027-3.037-1.852-3.037-1.853 0-2.136 1.445-2.136 2.939v5.667H9.351V9h3.414v1.561h.046c.477-.9 1.637-1.85 3.37-1.85 3.601 0 4.267 2.37 4.267 5.455v6.286zM5.337 7.433c-1.144 0-2.063-.926-2.063-2.065 0-1.138.92-2.063 2.063-2.063 1.14 0 2.064.925 2.064 2.063 0 1.139-.925 2.065-2.064 2.065zm1.782 13.019H3.555V9h3.564v11.452zM22.225 0H1.771C.792 0 0 .774 0 1.729v20.542C0 23.227.792 24 1.771 24h20.451C23.2 24 24 23.227 24 22.271V1.729C24 .774 23.2 0 22.222 0h.003z"/>
              </svg>
            </a>
          </div>
        </div>
      </div>
      
      <div class="footer-bottom">
        <p class="footer-copyright">KINDER SCAPES © 2025. All rights reserved.</p>
      </div>
    </div>
  </footer>
</template>

<script setup>
const scrollToHome = () => {
  const element = document.getElementById('home')
  if (element) {
    element.scrollIntoView({ 
      behavior: 'smooth',
      block: 'start'
    })
  }
}
</script>

<style scoped>
.footer {
  background: var(--primary-dark-blue);
  color: var(--white);
  padding: 60px 20px 30px;
}

.footer-content {
  display: grid;
  grid-template-columns: 2fr 1fr 1fr 1fr;
  gap: 48px;
  margin-bottom: 48px;
}

.footer-logo {
  display: flex;
  align-items: center;
  gap: 16px;
  margin-bottom: 20px;
  text-decoration: none;
  cursor: pointer;
  transition: opacity 0.3s ease;
}

.footer-logo:hover {
  opacity: 0.9;
}

.footer-logo-image {
  width: 60px;
  height: 60px;
  object-fit: contain;
}

.footer-logo-text {
  display: flex;
  flex-direction: column;
  gap: 2px;
}

.footer-logo-title {
  font-size: 1.5rem;
  font-weight: 700;
  color: var(--white);
  line-height: 1.2;
  letter-spacing: 0.5px;
}

.footer-logo-tagline {
  font-size: 0.75rem;
  font-weight: 400;
  color: rgba(255, 255, 255, 0.8);
  line-height: 1.2;
  letter-spacing: 0.3px;
}

.footer-description {
  color: rgba(255, 255, 255, 0.7);
  line-height: 1.7;
  max-width: 300px;
}

.footer-heading {
  font-size: 1rem;
  font-weight: 700;
  margin-bottom: 20px;
  color: var(--white);
}

.footer-links {
  list-style: none;
  display: flex;
  flex-direction: column;
  gap: 12px;
}

.footer-links a {
  color: rgba(255, 255, 255, 0.7);
  text-decoration: none;
  transition: color 0.3s ease;
}

.footer-links a:hover {
  color: var(--white);
}

.social-icons {
  display: flex;
  gap: 16px;
}

.social-icon {
  width: 40px;
  height: 40px;
  background: rgba(255, 255, 255, 0.1);
  border-radius: 8px;
  display: flex;
  align-items: center;
  justify-content: center;
  color: var(--white);
  transition: all 0.3s ease;
}

.social-icon:hover {
  background: rgba(255, 255, 255, 0.2);
  transform: translateY(-2px);
}

.footer-bottom {
  border-top: 1px solid rgba(255, 255, 255, 0.1);
  padding-top: 24px;
}

.footer-copyright {
  color: rgba(255, 255, 255, 0.5);
  font-size: 0.875rem;
}

@media (max-width: 1024px) {
  .footer-content {
    grid-template-columns: 1fr 1fr;
  }
  
  .footer-logo {
    gap: 12px;
  }
  
  .footer-logo-image {
    width: 50px;
    height: 50px;
  }
  
  .footer-logo-title {
    font-size: 1.25rem;
  }
  
  .footer-logo-tagline {
    font-size: 0.7rem;
  }
}

@media (max-width: 768px) {
  .footer-content {
    grid-template-columns: 1fr;
    gap: 32px;
  }
  
  .footer-logo {
    gap: 10px;
  }
  
  .footer-logo-image {
    width: 45px;
    height: 45px;
  }
  
  .footer-logo-title {
    font-size: 1.1rem;
  }
  
  .footer-logo-tagline {
    font-size: 0.65rem;
  }
}
</style>


