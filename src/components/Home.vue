<script setup>
// You can add any script logic here if needed
</script>

<template>
  <div class="welcome-container">
    <div class="welcome-header">
      <h1 class="welcome-title">Welcome to Momo Admin</h1>
      <p class="welcome-subtitle">Your powerful dashboard for managing payments and users</p>
    </div>

    <div class="dashboard-preview">
      <div class="preview-item">
        <div class="preview-icon"><i class="fa-solid fa-credit-card"></i></div>
        <div class="preview-title">Transactions</div>
        <div class="preview-desc">View & manage payments</div>
      </div>
      <div class="preview-item">
        <div class="preview-icon">👥</div>
        <div class="preview-title">Users</div>
        <div class="preview-desc">Manage user accounts</div>
      </div>
      <div class="preview-item">
        <div class="preview-icon">📊</div>
        <div class="preview-title">Analytics</div>
        <div class="preview-desc">View performance stats</div>
      </div>
      <div class="preview-item">
        <div class="preview-icon">⚙️</div>
        <div class="preview-title">Settings</div>
        <div class="preview-desc">Configure your system</div>
      </div>
      <div class="preview-item">
        <div class="preview-icon">🔒</div>
        <div class="preview-title">Security</div>
        <div class="preview-desc">Manage access controls</div>
      </div>
      <div class="preview-item">
        <div class="preview-icon">📝</div>
        <div class="preview-title">Reports</div>
        <div class="preview-desc">Generate custom reports</div>
      </div>
    </div>

    <div class="momo-wave"></div>
  </div>
</template>
<!--
<style>
:root {
  --dark-blue: #0a2463;
  --medium-blue: #3e5c9a;
  --light-blue: #7ea3cc;
  --accent-blue: #1e90ff;
}

.welcome-container {
  position: fixed;
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;
  overflow: auto;
  color: white;
  font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
}

.background-image {
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background-image: url('https://m.yodycdn.com/blog/hinh-nen-thien-nhien-4k-yody-vn-56.jpg');
  background-size: cover;
  background-position: center;
  filter: blur(8px) brightness(0.7);
  z-index: -1;
}

.content-wrapper {
  max-width: 1200px;
  margin: 0 auto;
  padding: 2rem;
  min-height: 100vh;
  display: flex;
  flex-direction: column;
  justify-content: center;
}

.welcome-header {
  margin-bottom: 3rem;
  text-align: center;
}

.welcome-title {
  font-size: 3rem;
  margin-bottom: 1rem;
  background: linear-gradient(to right, var(--light-blue), var(--accent-blue));
  -webkit-background-clip: text;
  background-clip: text;
  color: transparent;
  text-shadow: 0 2px 4px rgba(0, 0, 0, 0.2);
}

.welcome-subtitle {
  font-size: 1.3rem;
  color: rgba(255, 255, 255, 0.9);
  margin-bottom: 1.5rem;
}

.dashboard-preview {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
  gap: 20px;
  margin-top: 2rem;
}

.preview-item {
  background: rgba(10, 36, 99, 0.7);
  backdrop-filter: blur(5px);
  border-radius: 15px;
  padding: 2rem;
  height: 180px;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  transition: all 0.3s ease;
  border: 1px solid rgba(126, 163, 204, 0.3);
  box-shadow: 0 8px 32px rgba(0, 0, 0, 0.2);
}

.preview-item:hover {
  transform: translateY(-8px);
  background: rgba(10, 36, 99, 0.9);
  box-shadow: 0 12px 40px rgba(30, 144, 255, 0.3);
  border-color: var(--accent-blue);
}

.preview-item::after {
  content: '';
  position: absolute;
  bottom: 0;
  left: 0;
  width: 100%;
  height: 4px;
  background: linear-gradient(to right, var(--light-blue), var(--accent-blue));
  transform: scaleX(0);
  transform-origin: left;
  transition: transform 0.4s ease-out;
}

.preview-item:hover::after {
  transform: scaleX(1);
}

.preview-icon {
  font-size: 2.5rem;
  margin-bottom: 1rem;
  color: var(--accent-blue);
}

.preview-title {
  font-weight: 600;
  margin-bottom: 0.5rem;
  font-size: 1.2rem;
  color: white;
}

.preview-desc {
  font-size: 0.9rem;
  color: rgba(255, 255, 255, 0.7);
  text-align: center;
}

@media (max-width: 768px) {
  .content-wrapper {
    padding: 1.5rem;
  }

  .welcome-title {
    font-size: 2.2rem;
  }

  .welcome-subtitle {
    font-size: 1.1rem;
  }

  .dashboard-preview {
    grid-template-columns: 1fr;
  }

  .preview-item {
    height: 150px;
    padding: 1.5rem;
  }
}
</style>
-->