<template>
  <footer class="footer">
    <div class="container">
      <div class="footer-content">
        <div class="footer-column">
          <div class="footer-logo">
            <img src="/src/assets/kinder logo.png" alt="Kinder Scapes Logo" class="footer-logo-image" />
            <div class="footer-logo-text">
              <div class="footer-logo-title">KINDER SCAPES</div>
              <div class="footer-logo-tagline">DAYCARE MANAGEMENT SOFTWARE</div>
            </div>
          </div>
          <p class="footer-description">
            Empowering educators and caregivers to create a warm & nurturing environment for children with less paperwork.
          </p>
        </div>
        
        <div class="footer-column">
          <h4 class="footer-heading">Explore</h4>
          <ul class="footer-links">
            <li><a href="#features">Feature</a></li>
            <li><a href="#who-to-use">Who to use</a></li>
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
            <a href="#" class="social-icon">
              <svg width="24" height="24" viewBox="0 0 24 24" fill="currentColor">
                <path d="M24 4.557c-.883.392-1.832.656-2.828.775 1.017-.609 1.798-1.574 2.165-2.724-.951.564-2.005.974-3.127 1.195-.897-.957-2.178-1.555-3.594-1.555-3.179 0-5.515 2.966-4.797 6.045-4.091-.205-7.719-2.165-10.148-5.144-1.29 2.213-.669 5.108 1.523 6.574-.806-.026-1.566-.247-2.229-.616-.054 2.281 1.581 4.415 3.949 4.89-.693.188-1.452.232-2.224.084.626 1.956 2.444 3.379 4.6 3.419-2.07 1.623-4.678 2.348-7.29 2.04 2.179 1.397 4.768 2.212 7.548 2.212 9.142 0 14.307-7.721 13.995-14.646.962-.695 1.797-1.562 2.457-2.549z"/>
              </svg>
            </a>
            <a href="#" class="social-icon">
              <svg width="24" height="24" viewBox="0 0 24 24" fill="currentColor">
                <path d="M22.46 6c-.77.35-1.6.58-2.46.69.88-.53 1.56-1.37 1.88-2.38-.83.5-1.75.85-2.72 1.05C18.37 4.5 17.26 4 16 4c-2.35 0-4.27 1.92-4.27 4.29 0 .34.04.67.11.98C8.28 9.09 5.11 7.38 3 4.79c-.37.63-.58 1.37-.58 2.15 0 1.49.75 2.81 1.91 3.56-.71 0-1.37-.2-1.95-.5v.03c0 2.08 1.48 3.82 3.44 4.21a4.22 4.22 0 0 1-1.93.07 4.28 4.28 0 0 0 4 2.98 8.521 8.521 0 0 1-5.33 1.84c-.34 0-.68-.02-1.02-.06C3.44 20.29 5.7 21 8.12 21 16 21 20.33 14.46 20.33 8.79c0-.19 0-.37-.01-.56.84-.6 1.56-1.36 2.14-2.23z"/>
              </svg>
            </a>
            <a href="#" class="social-icon">
              <svg width="24" height="24" viewBox="0 0 24 24" fill="currentColor">
                <path d="M12 0C5.374 0 0 5.373 0 12 0 17.302 3.438 21.8 8.207 23.387c.599.111.793-.261.793-.577v-2.234c-3.338.726-4.033-1.416-4.033-1.416-.546-1.387-1.333-1.756-1.333-1.756-1.089-.745.083-.729.083-.729 1.205.084 1.839 1.237 1.839 1.237 1.07 1.834 2.807 1.304 3.492.997.107-.775.418-1.305.762-1.604-2.665-.305-5.467-1.334-5.467-5.931 0-1.311.469-2.381 1.236-3.221-.124-.303-.535-1.524.117-3.176 0 0 1.008-.322 3.301 1.23A11.509 11.509 0 0112 5.803c1.02.005 2.047.138 3.006.404 2.291-1.552 3.297-1.23 3.297-1.23.653 1.653.242 2.874.118 3.176.77.84 1.235 1.911 1.235 3.221 0 4.609-2.807 5.624-5.479 5.921.43.372.823 1.102.823 2.222v3.293c0 .319.192.694.801.576C20.566 21.797 24 17.3 24 12c0-6.627-5.373-12-12-12z"/>
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


