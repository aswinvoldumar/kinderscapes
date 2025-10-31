<template>
  <section class="analyze-data">
    <div class="container">
      <div class="analyze-content">
        <div class="analyze-text">
          <h2 class="analyze-title">
            Analyze our data in a few clicks without too many settings
          </h2>
          
          <ul class="analyze-features">
            <li class="feature-item">
              <span class="feature-icon"><svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1" stroke="currentColor" class="size-6">
  <path stroke-linecap="round" stroke-linejoin="round" d="M7.5 14.25v2.25m3-4.5v4.5m3-6.75v6.75m3-9v9M6 20.25h12A2.25 2.25 0 0 0 20.25 18V6A2.25 2.25 0 0 0 18 3.75H6A2.25 2.25 0 0 0 3.75 6v12A2.25 2.25 0 0 0 6 20.25Z" />
</svg>

</span>
              <span>Daily attendance and check-in patterns</span>
            </li>
            <li class="feature-item">
              <span class="feature-icon"><svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1" stroke="currentColor" class="size-6">
  <path stroke-linecap="round" stroke-linejoin="round" d="M12 6v12m-3-2.818.879.659c1.171.879 3.07.879 4.242 0 1.172-.879 1.172-2.303 0-3.182C13.536 12.219 12.768 12 12 12c-.725 0-1.45-.22-2.003-.659-1.106-.879-1.106-2.303 0-3.182s2.9-.879 4.006 0l.415.33M21 12a9 9 0 1 1-18 0 9 9 0 0 1 18 0Z" />
</svg>
</span>
              <span>Fee collection and pending payments</span>
            </li>
            <li class="feature-item">
              <span class="feature-icon"><svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1" stroke="currentColor" class="size-6">
  <path stroke-linecap="round" stroke-linejoin="round" d="M2.25 18 9 11.25l4.306 4.306a11.95 11.95 0 0 1 5.814-5.518l2.74-1.22m0 0-5.94-2.281m5.94 2.28-2.28 5.941" />
</svg>
</span>
              <span>Staff performance and child engagement</span>
            </li>
            <li class="feature-item">
              <span class="feature-icon"><svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1" stroke="currentColor" class="size-6">
  <path stroke-linecap="round" stroke-linejoin="round" d="M2.25 8.25h19.5M2.25 9h19.5m-16.5 5.25h6m-6 2.25h3m-3.75 3h15a2.25 2.25 0 0 0 2.25-2.25V6.75A2.25 2.25 0 0 0 19.5 4.5h-15a2.25 2.25 0 0 0-2.25 2.25v10.5A2.25 2.25 0 0 0 4.5 19.5Z" />
</svg>
</span>
              <span>Payment & billing overview</span>
            </li>
            <li class="feature-item">
              <span class="feature-icon"><svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1" stroke="currentColor" class="size-6">
  <path stroke-linecap="round" stroke-linejoin="round" d="M6.75 3v2.25M17.25 3v2.25M3 18.75V7.5a2.25 2.25 0 0 1 2.25-2.25h13.5A2.25 2.25 0 0 1 21 7.5v11.25m-18 0A2.25 2.25 0 0 0 5.25 21h13.5A2.25 2.25 0 0 0 21 18.75m-18 0v-7.5A2.25 2.25 0 0 1 5.25 9h13.5A2.25 2.25 0 0 1 21 11.25v7.5m-9-6h.008v.008H12v-.008ZM12 15h.008v.008H12V15Zm0 2.25h.008v.008H12v-.008ZM9.75 15h.008v.008H9.75V15Zm0 2.25h.008v.008H9.75v-.008ZM7.5 15h.008v.008H7.5V15Zm0 2.25h.008v.008H7.5v-.008Zm6.75-4.5h.008v.008h-.008v-.008Zm0 2.25h.008v.008h-.008V15Zm0 2.25h.008v.008h-.008v-.008Zm2.25-4.5h.008v.008H16.5v-.008Zm0 2.25h.008v.008H16.5V15Z" />
</svg>
</span>
              <span>Event & activity tracking</span>
            </li>
          </ul>
        </div>
        
        <div class="table-slider-container">
          <div class="table-slider-wrapper" :style="{ transform: `translateX(-${currentIndex * (100 / 3)}%)` }">
            <div class="table-card">
              <div class="table-header">
                <h4>Attendance Overview</h4>
              </div>
              <table class="data-table">
                <thead>
                  <tr>
                    <th>Name</th>
                    <th>Status</th>
                    <th>Present</th>
                  </tr>
                </thead>
                <tbody>
                  <tr>
                    <td>Sofia Nasom</td>
                    <td>Present</td>
                    <td>✓</td>
                  </tr>
                  <tr>
                    <td>Emma Wilson</td>
                    <td>Present</td>
                    <td>✓</td>
                  </tr>
                  <tr>
                    <td>James Brown</td>
                    <td>Absent</td>
                    <td>-</td>
                  </tr>
                  <tr>
                    <td>Olivia Davis</td>
                    <td>Present</td>
                    <td>✓</td>
                  </tr>
                </tbody>
              </table>
            </div>
            
            <div class="table-card">
              <div class="table-header">
                <h4>Payment Status</h4>
              </div>
              <table class="data-table">
                <thead>
                  <tr>
                    <th>Child</th>
                    <th>Due Date</th>
                    <th>Status</th>
                  </tr>
                </thead>
                <tbody>
                  <tr>
                    <td>Alex Johnson</td>
                    <td>15 Jan</td>
                    <td class="paid">Paid</td>
                  </tr>
                  <tr>
                    <td>Mia Anderson</td>
                    <td>15 Jan</td>
                    <td class="pending">Pending</td>
                  </tr>
                  <tr>
                    <td>Noah Taylor</td>
                    <td>20 Jan</td>
                    <td class="paid">Paid</td>
                  </tr>
                  <tr>
                    <td>Lily Martinez</td>
                    <td>20 Jan</td>
                    <td class="pending">Pending</td>
                  </tr>
                </tbody>
              </table>
            </div>
            
            <div class="table-card">
              <div class="table-header">
                <h4>Activity Summary</h4>
              </div>
              <table class="data-table">
                <thead>
                  <tr>
                    <th>Activity</th>
                    <th>Count</th>
                    <th>Status</th>
                  </tr>
                </thead>
                <tbody>
                  <tr>
                    <td>Art & Craft</td>
                    <td>15</td>
                    <td class="active">Active</td>
                  </tr>
                  <tr>
                    <td>Music Class</td>
                    <td>12</td>
                    <td class="active">Active</td>
                  </tr>
                  <tr>
                    <td>Outdoor Play</td>
                    <td>8</td>
                    <td class="inactive">Inactive</td>
                  </tr>
                  <tr>
                    <td>Story Time</td>
                    <td>20</td>
                    <td class="active">Active</td>
                  </tr>
                </tbody>
              </table>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
import { ref, onMounted, onUnmounted } from 'vue'

const currentIndex = ref(0)
let slideInterval = null

const nextSlide = () => {
  currentIndex.value = (currentIndex.value + 1) % 3
}

onMounted(() => {
  // Change slides every 5 seconds
  slideInterval = setInterval(nextSlide, 5000)
})

onUnmounted(() => {
  if (slideInterval) {
    clearInterval(slideInterval)
  }
})
</script>

<style scoped>
.analyze-data {
  padding: var(--section-padding);
  background: linear-gradient(135deg, var(--primary-dark-blue) 0%, var(--primary-blue) 100%);
  color: var(--white);
}

.analyze-content {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 60px;
  align-items: center;
}

.analyze-title {
  font-size: var(--font-size-h2);
  font-weight: 800;
  color: var(--white);
  margin-bottom: 48px;
  line-height: 1.3;
}

.analyze-features {
  list-style: none;
  display: flex;
  flex-direction: column;
  gap: 24px;
}

.feature-item {
  display: flex;
  align-items: center;
  gap: 16px;
  font-size: 1.125rem;
}

.feature-icon {
  font-size: 1.5rem;
  width: 40px;
  height: 40px;
  display: flex;
  align-items: center;
  justify-content: center;
  background: rgba(255, 255, 255, 0.1);
  border-radius: 8px;
}

.table-slider-container {
  border-radius: 20px;
  overflow: hidden;
  position: relative;
}

.table-slider-wrapper {
  display: flex;
  width: 300%;
  transition: transform 0.5s ease-in-out;
}

.table-card {
  background: var(--white);
  border-radius: 16px;
  padding: 24px;
  box-shadow: 0 10px 40px rgba(0, 0, 0, 0.2);
  flex: 0 0 50%;
  margin-right: 24px;
  min-width: 0;
}

.table-header {
  display: flex;
  justify-content: space-between;
  align-items: center;
  margin-bottom: 20px;
}

.table-header h4 {
  font-size: 1rem;
  font-weight: 600;
  color: var(--primary-dark-blue);
}

.data-table {
  width: 100%;
  border-collapse: collapse;
}

.data-table thead {
  border-bottom: 2px solid #e5e7eb;
}

.data-table th {
  text-align: left;
  padding: 12px 8px;
  font-size: 0.875rem;
  font-weight: 600;
  color: var(--primary-dark-blue);
  text-transform: uppercase;
  letter-spacing: 0.5px;
}

.data-table td {
  padding: 12px 8px;
  font-size: 0.95rem;
  color: var(--gray-dark);
  border-bottom: 1px solid #f3f4f6;
}

.data-table tbody tr:hover {
  background-color: #f8fafc;
}

.data-table td.paid {
  color: var(--accent-green);
  font-weight: 600;
}

.data-table td.pending {
  color: var(--accent-orange);
  font-weight: 600;
}

.data-table td.active {
  color: var(--accent-green);
  font-weight: 600;
}

.data-table td.inactive {
  color: var(--gray);
  font-weight: 600;
}

@media (max-width: 1024px) {
  .analyze-content {
    grid-template-columns: 1fr;
  }
  
  .table-slider-container {
    order: 1;
  }
  
  .analyze-text {
    order: 2;
  }
  
  .table-card {
    flex: 0 0 50%;
  }
}

@media (max-width: 768px) {
  .table-card {
    flex: 0 0 100%;
  }
  
  .data-table th,
  .data-table td {
    padding: 8px 4px;
    font-size: 0.875rem;
  }
}
</style>


