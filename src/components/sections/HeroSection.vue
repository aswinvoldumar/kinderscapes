<template>
  <section class="hero">
    <!-- Animated Background Elements -->
    <div class="background-elements">
      <!-- Stars -->
      <div class="star star-1"></div>
      <div class="star star-2"></div>
      <div class="star star-3"></div>
      <div class="star star-4"></div>
      <div class="star star-5"></div>
      <div class="star star-6"></div>
      <div class="star star-7"></div>
      <div class="star star-8"></div>
      
      <!-- Animated Clouds -->
      <div class="cloud cloud-1">
        <svg width="172" height="125" viewBox="0 0 172 125" fill="none" xmlns="http://www.w3.org/2000/svg">
          <path d="M42.8406 124.5C31.027 124.5 20.9335 120.415 12.5601 112.245C4.18669 104.074 0 94.0883 0 82.2867C0 72.1711 3.05077 63.1578 9.15231 55.2469C15.2538 47.3359 23.2378 42.2781 33.1041 40.0734C36.3496 28.1422 42.8406 18.4805 52.5771 11.0883C62.3136 3.69609 73.3483 0 85.6812 0C100.87 0 113.755 5.28477 124.335 15.8543C134.915 26.4238 140.206 39.2953 140.206 54.4688C149.163 55.5063 156.595 59.3645 162.502 66.0434C168.409 72.7223 171.362 80.5359 171.362 89.4844C171.362 99.2109 167.955 107.479 161.139 114.287C154.323 121.096 146.047 124.5 136.311 124.5H42.8406Z" fill="white" fill-opacity="0.07"/>
        </svg>
      </div>
      
      <div class="cloud cloud-2">
        <svg width="172" height="125" viewBox="0 0 172 125" fill="none" xmlns="http://www.w3.org/2000/svg">
          <path d="M42.8406 124.5C31.027 124.5 20.9335 120.415 12.5601 112.245C4.18669 104.074 0 94.0883 0 82.2867C0 72.1711 3.05077 63.1578 9.15231 55.2469C15.2538 47.3359 23.2378 42.2781 33.1041 40.0734C36.3496 28.1422 42.8406 18.4805 52.5771 11.0883C62.3136 3.69609 73.3483 0 85.6812 0C100.87 0 113.755 5.28477 124.335 15.8543C134.915 26.4238 140.206 39.2953 140.206 54.4688C149.163 55.5063 156.595 59.3645 162.502 66.0434C168.409 72.7223 171.362 80.5359 171.362 89.4844C171.362 99.2109 167.955 107.479 161.139 114.287C154.323 121.096 146.047 124.5 136.311 124.5H42.8406Z" fill="white" fill-opacity="0.07"/>
        </svg>
      </div>
    </div>
    
    <div class="container">
      <div class="hero-content">
        <div class="hero-text">
          <span class="hero-label">Leading Daycare Management Software</span>
          <h1 class="hero-title">Manage your Day Care with easy and joy</h1>
          <div class="hero-input-group">
            <input type="email" placeholder="Input your mail..." class="hero-input" />
            <button class="btn-secondary">
              Try for Free
            </button>
          </div>
        </div>
      </div>
    </div>
    
    <div class="dashboard-container">
      <img src="/src/assets/dashboard.png" alt="Dashboard Preview" class="dashboard-image" />
    </div>
  </section>
</template>

<script setup>
</script>

<style scoped>
.hero {
  background-image: url('/src/assets/hero background.png');
  background-size: cover;
  background-position: center;
  background-repeat: no-repeat;
  padding: 120px 20px 0;
  position: relative;
  overflow: visible;
  height: 100vh;
 
}

.hero::before {
  content: '';
  position: absolute;
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;
  background: rgba(0, 0, 0, 0.3);
  pointer-events: none;
}

.background-elements {
  position: absolute;
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;
  pointer-events: none;
  z-index: 1;
}

/* Stars */
.star {
  position: absolute;
  background: rgba(255, 255, 255, 0.8);
  border-radius: 50%;
  animation: twinkle 3s ease-in-out infinite;
}

.star-1 {
  width: 4px;
  height: 4px;
  top: 20%;
  left: 10%;
  animation-delay: 0s;
}

.star-2 {
  width: 6px;
  height: 6px;
  top: 15%;
  left: 85%;
  animation-delay: 0.5s;
}

.star-3 {
  width: 3px;
  height: 3px;
  top: 30%;
  left: 20%;
  animation-delay: 1s;
}

.star-4 {
  width: 5px;
  height: 5px;
  top: 25%;
  left: 75%;
  animation-delay: 1.5s;
}

.star-5 {
  width: 4px;
  height: 4px;
  top: 40%;
  left: 5%;
  animation-delay: 2s;
}

.star-6 {
  width: 3px;
  height: 3px;
  top: 35%;
  left: 90%;
  animation-delay: 2.5s;
}

.star-7 {
  width: 5px;
  height: 5px;
  top: 50%;
  left: 15%;
  animation-delay: 0.8s;
}

.star-8 {
  width: 4px;
  height: 4px;
  top: 45%;
  left: 80%;
  animation-delay: 1.8s;
}


/* Cloud Styles */
.cloud {
  position: absolute;
  pointer-events: none;
  z-index: 1;
}

.cloud-1 {
  top: 20%;
  left: 20%;
  width: 120px;
  height: 87px;
  animation: floatCloud1 20s ease-in-out infinite;
}

.cloud-2 {
  top: 50%;
  right: 20%;
  width: 100px;
  height: 73px;
  animation: floatCloud2 25s ease-in-out infinite;
}

.cloud svg {
  width: 100%;
  height: 100%;
  filter: drop-shadow(0 4px 8px rgba(255, 255, 255, 0.1));
}

/* Animations */
@keyframes twinkle {
  0%, 100% {
    opacity: 0.3;
    transform: scale(1);
  }
  50% {
    opacity: 1;
    transform: scale(1.2);
  }
}

@keyframes floatCloud1 {
  0% {
    transform: translateX(-50px) translateY(0px) rotate(0deg);
    opacity: 0.3;
  }
  25% {
    transform: translateX(20px) translateY(-10px) rotate(1deg);
    opacity: 0.6;
  }
  50% {
    transform: translateX(50px) translateY(5px) rotate(0deg);
    opacity: 0.8;
  }
  75% {
    transform: translateX(80px) translateY(-5px) rotate(-1deg);
    opacity: 0.6;
  }
  100% {
    transform: translateX(120px) translateY(0px) rotate(0deg);
    opacity: 0.3;
  }
}

@keyframes floatCloud2 {
  0% {
    transform: translateX(50px) translateY(0px) rotate(0deg);
    opacity: 0.3;
  }
  25% {
    transform: translateX(-20px) translateY(10px) rotate(-1deg);
    opacity: 0.6;
  }
  50% {
    transform: translateX(-50px) translateY(-5px) rotate(0deg);
    opacity: 0.8;
  }
  75% {
    transform: translateX(-80px) translateY(5px) rotate(1deg);
    opacity: 0.6;
  }
  100% {
    transform: translateX(-120px) translateY(0px) rotate(0deg);
    opacity: 0.3;
  }
}


.hero-content {
  display: flex;
  justify-content: center;
  align-items: center;
  position: relative;
  z-index: 2;
  text-align: center;
}

.hero-text {
  display: flex;
  flex-direction: column;
  gap: 24px;
  align-items: center;
  max-width: 800px;
}

.hero-label {margin-top: 20px;
  color: var(--white);
  opacity: 0.9;
  font-size: 1rem;
  font-weight: 200;
  text-transform: uppercase;
  letter-spacing: 1px;
}

.hero-title {
  font-size: 3.5rem;
  font-weight: 800;
  color: var(--white);
  line-height: 1.1;
  margin: 0;
}

.hero-input-group {
  display: flex;
  gap: 16px;
  align-items: center;
  max-width: 500px;
  width: 100%;
  margin-top: 16px;
}

.hero-input {
  flex: 1;
  padding: 16px 20px;
  border: none;
  border-radius: 8px;
  font-size: 1rem;
  font-family: inherit;
  outline: none;
  background: var(--white);
  color: var(--gray-dark);
}

.hero-input::placeholder {
  color: #64748b;
}

.btn-secondary {
  background-color: var(--white);
  color: var(--primary-dark-blue);
  padding: 16px 32px;
  border: none;
  border-radius: 8px;
  font-size: 1rem;
  font-weight: 600;
  cursor: pointer;
  transition: all 0.3s ease;
  white-space: nowrap;
}

.btn-secondary:hover {
  background-color: rgba(255, 255, 255, 0.95);
  transform: translateY(-2px);
}

.dashboard-container {
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translateX(-50%);
  display: flex;
  justify-content: center;
  z-index: 10;
}

.dashboard-image {
  max-width: 1000px;
  width: 100%;
  height: auto;
  border-radius: 16px;
  transform: perspective(1000px) rotateY(-2deg);
}

/* Tablet and smaller desktop */
@media (max-width: 1024px) {
  .hero {
    height: 100vh;
    min-height: 700px;
    padding: 100px 20px 0;
  }
  
  .hero-title {
    font-size: 2.5rem;
    line-height: 1.2;
  }
  
  .hero-text {
    max-width: 600px;
    gap: 20px;
  }
  
  .hero-input-group {
    max-width: 400px;
  }
  
  .dashboard-container {
    top: 70%;
  }
  
  .dashboard-image {
    max-width: 800px;
    transform: none;
  }
  
  /* Adjust cloud sizes for tablets */
  .cloud-1 {
    width: 100px;
    height: 73px;
  }
  
  .cloud-2 {
    width: 85px;
    height: 62px;
  }
}

/* Mobile landscape and small tablets */
@media (max-width: 768px) {
  .hero {
    height: 100vh;
    min-height: 600px;
    padding: 80px 15px 0;
  }
  
  .hero-content {
    padding: 0 10px;
  }
  
  .hero-text {
    max-width: 100%;
    gap: 18px;
  }
  
  .hero-label {
    font-size: 0.9rem;
    margin-top: 10px;
  }
  
  .hero-title {
    font-size: 2rem;
    line-height: 1.3;
    padding: 0 10px;
  }
  
  .hero-input-group {
    flex-direction: column;
    max-width: 100%;
    gap: 12px;
    margin-top: 12px;
  }
  
  .hero-input {
    width: 100%;
    padding: 14px 16px;
    font-size: 0.95rem;
  }
  
  .btn-secondary {
    width: 100%;
    padding: 14px 24px;
    font-size: 0.95rem;
  }
  
  .dashboard-container {
    top: 65%;
    padding: 0 10px;
  }
  
  .dashboard-image {
    max-width: 100%;
    width: 100%;
  }
  
  /* Adjust cloud sizes for mobile */
  .cloud-1 {
    width: 90px;
    height: 66px;
    top: 12%;
  }
  
  .cloud-2 {
    width: 75px;
    height: 55px;
    top: 20%;
  }
}

/* Mobile portrait */
@media (max-width: 480px) {
  .hero {
    height: 100vh;
    min-height: 500px;
    padding: 60px 10px 0;
  }
  
  .hero-content {
    padding: 0 5px;
  }
  
  .hero-text {
    gap: 16px;
  }
  
  .hero-label {
    font-size: 0.85rem;
    margin-top: 5px;
    letter-spacing: 0.5px;
  }
  
  .hero-title {
    font-size: 1.75rem;
    line-height: 1.4;
    padding: 0 5px;
  }
  
  .hero-input-group {
    gap: 10px;
    margin-top: 10px;
  }
  
  .hero-input {
    padding: 12px 14px;
    font-size: 0.9rem;
  }
  
  .btn-secondary {
    padding: 12px 20px;
    font-size: 0.9rem;
  }
  
  .dashboard-container {
    top: 60%;
    padding: 0 5px;
  }
  
  .dashboard-image {
    border-radius: 12px;
  }
}

/* Extra small mobile devices */
@media (max-width: 360px) {
  .hero {
    padding: 50px 8px 0;
  }
  
  .hero-content {
    padding: 0 2px;
  }
  
  .hero-text {
    gap: 14px;
  }
  
  .hero-label {
    font-size: 0.8rem;
  }
  
  .hero-title {
    font-size: 1.5rem;
    line-height: 1.5;
  }
  
  .hero-input-group {
    gap: 8px;
  }
  
  .hero-input {
    padding: 10px 12px;
    font-size: 0.85rem;
  }
  
  .btn-secondary {
    padding: 10px 16px;
    font-size: 0.85rem;
  }
  
  .dashboard-container {
    top: 55%;
  }
  
  /* Smaller stars on very small screens */
  .star {
    width: 2px !important;
    height: 2px !important;
  }
  
  .star-2, .star-4, .star-7 {
    width: 3px !important;
    height: 3px !important;
  }
  
  /* Smaller clouds on very small screens */
  .cloud-1 {
    width: 80px;
    height: 58px;
  }
  
  .cloud-2 {
    width: 70px;
    height: 51px;
  }
}

/* Landscape mobile orientation */
@media (max-height: 500px) and (orientation: landscape) {
  .hero {
    height: auto;
    min-height: 100vh;
    padding: 40px 20px 0;
  }
  
  .hero-text {
    gap: 12px;
  }
  
  .hero-title {
    font-size: 1.5rem;
  }
  
  .hero-input-group {
    flex-direction: row;
    max-width: 400px;
  }
  
  .dashboard-container {
    top: 80%;
  }
}
</style>

