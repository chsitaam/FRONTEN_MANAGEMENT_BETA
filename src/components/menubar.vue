<template>
  <div>
    <div class="menu-toggle" @click="toggleSidebar">
      <i class="fas fa-sliders-h"></i>
    </div>

    <div :class="['sidebar', { open: isSidebarOpen }]">
      <div class="logo-section">
        <img src="" alt="Logo" />
      </div>

      <div class="menu-items">
        <div class="menu-item">
          <i class="fas fa-home"></i>
          <span>Trang chủ</span>
        </div>

        <div class="menu-item" @click="toggleSubmenu('products')">
          <i class="fas fa-box"></i>
          <span>Quản lý Sản phẩm</span>
          <i :class="['fas fa-chevron-down chevron', { open: isProductsOpen }]"></i>
        </div>
        <div class="submenu" :class="{ open: isProductsOpen }">
          <div class="submenu-item">Danh mục sản phẩm</div>
          <div class="submenu-item">Sản phẩm</div>
        </div>

        <div class="menu-item">
          <i class="fa-solid fa-receipt"></i>
          <span>Đơn hàng</span>
        </div>

        <div class="menu-item">
          <i class="fa-solid fa-gift"></i>
          <span>Khuyến mãi</span>
        </div>

        <div class="menu-item">
          <i class="fa-solid fa-users"></i>
          <span>Người dùng</span>
        </div>

        <div class="menu-item">
          <i class="fa-solid fa-lock"></i>
          <span>Bảo mật</span>
        </div>

        <div class="menu-item">
          <i class="fa-solid fa-gift"></i>
          <span>Thống kê</span>
        </div>

        <div class="menu-item" @click="toggleSubmenu('documents')">
          <i class="fas fa-file-alt"></i>
          <span>Tài liệu</span>
          <i :class="['fas fa-chevron-down chevron', { open: isDocumentsOpen }]"></i>
        </div>
        <div class="submenu" :class="{ open: isDocumentsOpen }">
          <div class="submenu-item">Hướng dẫn sử dụng</div>
          <div class="submenu-item">Chính sách bảo mật</div>
        </div>
      </div>

      <div class="auth-section">
        <div class="auth-item login">
          <i class="fas fa-sign-in-alt"></i>
          <span>Đăng nhập</span>
        </div>
        <div class="auth-item logout"  @click="$emit('logout')">
          <i class="fas fa-sign-out-alt"></i>
          <span>Đăng xuất</span>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      isSidebarOpen: false,
      isProductsOpen: false,
      isDocumentsOpen: false,
    };
  },
  methods: {
    toggleSidebar() {
      this.isSidebarOpen = !this.isSidebarOpen;
      this.$emit('toggle', this.isSidebarOpen); // Thêm dòng này
    },
    toggleSubmenu(menu) {
      if (menu === 'products') {
        this.isProductsOpen = !this.isProductsOpen;
      } else if (menu === 'documents') {
        this.isDocumentsOpen = !this.isDocumentsOpen;
      }
    },
  },
};
</script>

<style scoped>

.menu-toggle {
  position: fixed;
  top: 20px;
  left: 20px;
  font-size: 24px;
  color: #3b82f6;
  cursor: pointer;
  z-index: 1001;
  transition: transform 0.3s;
}

.menu-toggle:hover {
  transform: scale(1.1);
}

.sidebar {
  position: fixed;
  top: 0;
  left: -250px;
  width: 250px;
  height: 100vh;
  background: white;
  transition: left 0.4s ease-out;
  z-index: 1000;
  display: flex;
  flex-direction: column;
}

.sidebar.open {
  left: 0;
}

.logo-section {
  padding: 20px;
  text-align: center;
}

.logo-section img {
  max-width: 120px;
  height: auto;
}

.menu-items {
  flex: 1;
  overflow-y: auto;
  padding: 10px 0;
}

.menu-item {
  padding: 12px 20px;
  color: #334155;
  cursor: pointer;
  transition: all 0.2s;
  display: flex;
  align-items: center;
  position: relative;
}

.menu-item:hover {
  color: #3b82f6;
}

.menu-item:hover::before {
  content: '';
  position: absolute;
  left: 0;
  top: 0;
  height: 100%;
  width: 3px;
  background-color: #3b82f6;
}

.menu-item i {
  margin-right: 12px;
  width: 20px;
  text-align: center;
}

.submenu {
  max-height: 0;
  overflow: hidden;
  transition: max-height 0.3s ease-out;
}

.submenu.open {
  max-height: 500px;
}

.submenu-item {
  padding: 10px 20px 10px 52px;
  color: #64748b;
  cursor: pointer;
  font-size: 14px;
}

.submenu-item:hover {
  color: #3b82f6;
  background-color: #f1f5f9;
}

.auth-section {
  margin-top: auto;
  padding: 15px 0;
  border-top: 1px solid #e2e8f0;
}

.auth-item {
  padding: 12px 20px;
  display: flex;
  align-items: center;
  cursor: pointer;
  font-size: 14px;
}

.auth-item.login {
  color: #3b82f6;
}

.auth-item.logout {
  color: #ef4444;
}

.auth-item i {
  margin-right: 12px;
}

.chevron {
  margin-left: auto;
  font-size: 12px;
  transition: transform 0.3s;
}

.chevron.open {
  transform: rotate(180deg);
}
</style>
