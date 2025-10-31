<template>
  <teleport to="body">
    <transition name="modal">
      <div v-if="isVisible" class="modal-overlay" @click.self="closeModal">
        <div class="modal-container">
          <button class="close-button" @click="closeModal">
            <svg width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2">
              <line x1="18" y1="6" x2="6" y2="18"></line>
              <line x1="6" y1="6" x2="18" y2="18"></line>
            </svg>
          </button>
          
          <div class="modal-content">
            <h2 class="modal-title">Start Your Free Trial</h2>
            <p class="modal-subtitle">Fill out the form below to get started</p>
            
            <form @submit.prevent="submitForm" class="trial-form">
              <div class="form-group">
                <label for="name">Full Name *</label>
                <input 
                  type="text" 
                  id="name"
                  v-model="formData.name" 
                  required 
                  placeholder="Enter your full name"
                  class="form-input"
                />
              </div>
              
              <div class="form-group">
                <label for="email">Email Address *</label>
                <input 
                  type="email" 
                  id="email"
                  v-model="formData.email" 
                  required 
                  placeholder="Enter your email address"
                  class="form-input"
                />
              </div>
              
              <div class="form-group">
                <label for="phone">Phone Number *</label>
                <input 
                  type="tel" 
                  id="phone"
                  v-model="formData.phone" 
                  required 
                  placeholder="Enter your phone number"
                  class="form-input"
                />
              </div>
              
              <button type="submit" class="submit-button" :disabled="isSubmitting">
                <span v-if="!isSubmitting">Submit Request</span>
                <span v-else>Sending...</span>
              </button>
            </form>
          </div>
          
          <div v-if="showSuccess" class="success-message">
            <div class="success-icon">
              <svg width="48" height="48" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2">
                <polyline points="20 6 9 17 4 12"></polyline>
              </svg>
            </div>
            <h3>Thank You!</h3>
            <p>Your free trial request has been submitted successfully. We'll get back to you soon!</p>
          </div>
        </div>
      </div>
    </transition>
  </teleport>
</template>

<script setup>
import { ref } from 'vue'

const props = defineProps({
  isVisible: {
    type: Boolean,
    default: false
  }
})

const emit = defineEmits(['close'])

const formData = ref({
  name: '',
  email: '',
  phone: ''
})

const isSubmitting = ref(false)
const showSuccess = ref(false)

const closeModal = () => {
  if (!isSubmitting.value) {
    showSuccess.value = false
    emit('close')
    // Reset form after animation
    setTimeout(() => {
      formData.value = {
        name: '',
        email: '',
        phone: ''
      }
    }, 300)
  }
}

const submitForm = async () => {
  isSubmitting.value = true
  
  try {
    // API endpoint from environment or default to localhost
    const apiUrl = import.meta.env.VITE_API_URL || 'http://localhost:3001'
    
    const response = await fetch(`${apiUrl}/api/free-trial`, {
      method: 'POST',
      headers: {
        'Content-Type': 'application/json',
      },
      body: JSON.stringify({
        name: formData.value.name,
        email: formData.value.email,
        phone: formData.value.phone
      })
    })

    const data = await response.json()

    if (!response.ok) {
      throw new Error(data.message || 'Failed to submit request')
    }
    
    // Show success message
    showSuccess.value = true
    
    // Close modal after 3 seconds
    setTimeout(() => {
      closeModal()
    }, 3000)
    
  } catch (error) {
    console.error('Failed to send email:', error)
    alert(error.message || 'Failed to send your request. Please try again later.')
  } finally {
    isSubmitting.value = false
  }
}
</script>

<style scoped>
.modal-overlay {
  position: fixed;
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;
  background: rgba(0, 0, 0, 0.6);
  backdrop-filter: blur(4px);
  display: flex;
  align-items: center;
  justify-content: center;
  z-index: 10000;
  padding: 20px;
}

.modal-container {
  background: var(--white);
  border-radius: 16px;
  max-width: 500px;
  width: 100%;
  max-height: 90vh;
  overflow-y: auto;
  position: relative;
  box-shadow: 0 20px 60px rgba(0, 0, 0, 0.3);
  animation: slideIn 0.3s ease-out;
}

@keyframes slideIn {
  from {
    opacity: 0;
    transform: translateY(-50px) scale(0.9);
  }
  to {
    opacity: 1;
    transform: translateY(0) scale(1);
  }
}

.close-button {
  position: absolute;
  top: 20px;
  right: 20px;
  background: transparent;
  border: none;
  cursor: pointer;
  padding: 8px;
  display: flex;
  align-items: center;
  justify-content: center;
  color: var(--gray);
  transition: all 0.3s ease;
  z-index: 10;
}

.close-button:hover {
  color: var(--primary-dark-blue);
  transform: rotate(90deg);
}

.modal-content {
  padding: 40px;
}

.modal-title {
  font-size: 2rem;
  font-weight: 800;
  color: var(--primary-dark-blue);
  margin-bottom: 8px;
  text-align: center;
}

.modal-subtitle {
  font-size: 1rem;
  color: var(--gray);
  margin-bottom: 32px;
  text-align: center;
}

.trial-form {
  display: flex;
  flex-direction: column;
  gap: 24px;
}

.form-group {
  display: flex;
  flex-direction: column;
  gap: 8px;
}

.form-group label {
  font-size: 0.95rem;
  font-weight: 600;
  color: var(--primary-dark-blue);
}

.form-input {
  padding: 14px 16px;
  border: 2px solid #e2e8f0;
  border-radius: 8px;
  font-size: 1rem;
  font-family: inherit;
  transition: all 0.3s ease;
  outline: none;
  background: var(--white);
}

.form-input:focus {
  border-color: var(--primary-light-blue);
  box-shadow: 0 0 0 3px rgba(16, 52, 130, 0.1);
}

.submit-button {
  background: var(--primary-light-blue);
  color: var(--white);
  padding: 16px 32px;
  border: none;
  border-radius: 8px;
  font-size: 1rem;
  font-weight: 600;
  cursor: pointer;
  transition: all 0.3s ease;
  margin-top: 8px;
}

.submit-button:hover:not(:disabled) {
  background: var(--primary-blue);
  transform: translateY(-2px);
  box-shadow: 0 4px 12px rgba(16, 52, 130, 0.3);
}

.submit-button:disabled {
  opacity: 0.6;
  cursor: not-allowed;
}

.success-message {
  position: absolute;
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;
  background: var(--white);
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  padding: 40px;
  text-align: center;
  border-radius: 16px;
  animation: fadeIn 0.3s ease-out;
}

@keyframes fadeIn {
  from {
    opacity: 0;
  }
  to {
    opacity: 1;
  }
}

.success-icon {
  width: 80px;
  height: 80px;
  background: var(--accent-green);
  border-radius: 50%;
  display: flex;
  align-items: center;
  justify-content: center;
  color: var(--white);
  margin-bottom: 24px;
}

.success-message h3 {
  font-size: 1.75rem;
  font-weight: 800;
  color: var(--primary-dark-blue);
  margin-bottom: 12px;
}

.success-message p {
  font-size: 1rem;
  color: var(--gray);
  line-height: 1.6;
  max-width: 400px;
}

/* Modal transitions */
.modal-enter-active,
.modal-leave-active {
  transition: opacity 0.3s ease;
}

.modal-enter-from,
.modal-leave-to {
  opacity: 0;
}

@media (max-width: 768px) {
  .modal-container {
    max-width: 100%;
    margin: 0;
    border-radius: 16px 16px 0 0;
    max-height: 95vh;
  }
  
  .modal-content {
    padding: 32px 24px;
  }
  
  .modal-title {
    font-size: 1.5rem;
  }
  
  .trial-form {
    gap: 20px;
  }
}

@media (max-width: 480px) {
  .modal-overlay {
    padding: 0;
  }
  
  .modal-container {
    border-radius: 0;
    max-height: 100vh;
  }
  
  .modal-content {
    padding: 24px 16px;
  }
  
  .close-button {
    top: 16px;
    right: 16px;
  }
  
  .success-message {
    padding: 24px;
  }
  
  .success-icon {
    width: 60px;
    height: 60px;
  }
  
  .success-icon svg {
    width: 32px;
    height: 32px;
  }
  
  .success-message h3 {
    font-size: 1.5rem;
  }
}
</style>

