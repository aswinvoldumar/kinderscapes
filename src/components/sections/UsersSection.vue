<template>
  <section class="users-section">
    <div class="container">
      <h2 class="section-title">Users</h2>
      <p class="section-subtitle">Choose your role to explore the dashboard and discover how Kinderscapes adapts to your specific needs</p>
      
      <div class="users-content">
        <!-- Left Side - User Login Options -->
        <div class="user-login-options">
          <div 
            v-for="userType in userTypes" 
            :key="userType.id"
            :class="['login-card', { 'active': selectedUser === userType.id }]"
            @click="selectUser(userType.id)"
          >
            <h3 class="login-title">{{ userType.title }}</h3>
            <p class="login-description">{{ userType.description }}</p>
          </div>
        </div>

        <!-- Right Side - Dynamic Dashboard Display -->
        <div class="dashboard-display">
          <div class="dashboard-container">
            <!-- Dynamic Dashboard Image based on selected user -->
            <div class="dashboard-image-container">
              <img 
                :src="dashboardImage" 
                :alt="dashboardAltText" 
                class="dashboard-image" 
              />
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
import { ref, computed } from 'vue'
import adminDashboard from '@/assets/dashboard admin.png'
import parentDashboard from '@/assets/dashboard parent.png'

const selectedUser = ref('admin')

const userTypes = [
  {
    id: 'admin',
    title: 'Admin Login',
    description: 'Full control of your daycare operations. Dashboard overview, Staff & Classroom Management Billing & Finance, Report & Analysis:'
  },
  {
    id: 'teachers',
    title: 'Teachers Login',
    description: 'Attendance Tracking. Activity Updates, Parent Communication, Classroom Planner.'
  },
  {
    id: 'parents',
    title: 'Parent Login',
    description: 'Daily Reports, Instant Messaging, Online Payments: Photo & Event Feed, Daily Activity checking'
  }
]

const selectUser = (userId) => {
  selectedUser.value = userId
}

// Computed property to get the correct dashboard image based on selected user
const dashboardImage = computed(() => {
  const imageMap = {
    admin: adminDashboard,
    teachers: parentDashboard, // Using parent image for teachers as no specific teacher image provided
    parents: parentDashboard
  }
  return imageMap[selectedUser.value] || adminDashboard
})

// Computed property for alt text
const dashboardAltText = computed(() => {
  const altMap = {
    admin: 'Admin Dashboard View',
    teachers: 'Teachers Dashboard View',
    parents: 'Parent Dashboard View'
  }
  return altMap[selectedUser.value] || 'Dashboard View'
})
</script>

<style scoped>
.users-section {
  padding: var(--section-padding);
  background: var(--white);
}

.section-title {
  font-size: var(--font-size-h2);
  font-weight: 800;
  color: var(--primary-dark-blue);
  text-align: center;
  margin-bottom: 16px;
}

.section-subtitle {
  font-size: 1.125rem;
  color: #64748b;
  text-align: center;
  max-width: 600px;
  margin: 0 auto 60px;
  line-height: 1.6;
}

.users-content {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 60px;
  align-items: start;
}

/* User Login Options */
.user-login-options {
  display: flex;
  flex-direction: column;
  gap: 24px;
}

.login-card {
  padding: 24px;
  border-radius: 16px;
  border: 2px solid #e2e8f0;
  background: var(--white);
  cursor: pointer;
  transition: all 0.4s cubic-bezier(0.4, 0, 0.2, 1);
  position: relative;
  overflow: hidden;
}

.login-card::before {
  content: '';
  position: absolute;
  top: 0;
  left: -100%;
  width: 100%;
  height: 100%;
  background: linear-gradient(90deg, transparent, rgba(255, 255, 255, 0.2), transparent);
  transition: left 0.5s ease;
}

.login-card:hover::before {
  left: 100%;
}

.login-card:hover {
  border-color: var(--primary-light-blue);
  transform: translateY(-2px);
  box-shadow: 0 8px 25px rgba(0, 0, 0, 0.1);
}

.login-card.active {
  border-color: var(--primary-blue);
  background: linear-gradient(135deg, var(--primary-blue) 0%, var(--primary-light-blue) 100%);
  color: var(--white);
  box-shadow: 0 10px 30px rgba(59, 130, 246, 0.3);
}

.login-card.active::before {
  content: '';
  position: absolute;
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;
  background: linear-gradient(135deg, var(--primary-blue) 0%, var(--primary-light-blue) 100%);
  border-radius: 14px;
  z-index: -1;
}

.login-title {
  font-size: 1.25rem;
  font-weight: 700;
  margin-bottom: 12px;
  color: inherit;
}

.login-description {
  font-size: 1rem;
  line-height: 1.6;
  color: inherit;
  opacity: 0.9;
}

/* Dashboard Display */
.dashboard-display {
  background: #f8fafc;
  border-radius: 20px;
  padding: 20px;
  box-shadow: 0 20px 60px rgba(0, 0, 0, 0.1);
}

/* Dashboard Image Container */
.dashboard-image-container {
  display: flex;
  justify-content: center;
  align-items: center;
  min-height: 400px;
  padding: 10px;
}

.dashboard-image {
  max-width: 100%;
  height: auto;
  border-radius: 12px;
  box-shadow: 0 10px 40px rgba(0, 0, 0, 0.15);
  transition: all 0.3s ease;
}

.dashboard-image:hover {
  transform: scale(1.02);
  box-shadow: 0 15px 50px rgba(0, 0, 0, 0.2);
}


/* Responsive Design */
@media (max-width: 1024px) {
  .users-content {
    grid-template-columns: 1fr;
    gap: 40px;
  }
  
  .dashboard-display {
    order: 1;
  }
  
  .user-login-options {
    order: 2;
  }
  
  .dashboard-image-container {
    min-height: 500px;
  }
}

@media (max-width: 768px) {
  .users-content {
    gap: 32px;
  }
  
  .dashboard-display {
    padding: 16px;
  }
  
  .dashboard-image-container {
    min-height: 400px;
    padding: 16px;
  }
  
}

@media (max-width: 480px) {
  .section-title {
    font-size: 2rem;
  }
  
  .login-card {
    padding: 20px;
  }
  
  .dashboard-image-container {
    min-height: 300px;
    padding: 12px;
  }
}
</style>

