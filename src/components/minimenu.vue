<template>
  <nav class="navbar">
    <div class="nav-logo">
      <img src="" alt="Logo" />
    </div>
    <ul class="nav-links">
      <li class="nav-item">
        <a href="#">Trang chủ</a>
      </li>

      <li class="nav-item dropdown" @mouseenter="openMenu('product')" @mouseleave="closeMenu('product')">
        <a href="#">Sản phẩm <i class="fas fa-chevron-down"></i></a>
        <ul class="dropdown-menu" v-show="open.product">
          <li><a href="#">Danh mục sản phẩm</a></li>
          <li><a href="#">Sản phẩm mới</a></li>
          <li><a href="#">Khuyến mãi</a></li>
        </ul>
      </li>

      <li class="nav-item">
        <a href="#">Giỏ hàng</a>
      </li>

      <li class="nav-item dropdown" @mouseenter="openMenu('docs')" @mouseleave="closeMenu('docs')">
        <a href="#">Tài liệu <i class="fas fa-chevron-down"></i></a>
        <ul class="dropdown-menu" v-show="open.docs">
          <li><a href="#">Hướng dẫn sử dụng</a></li>
          <li><a href="#">Chính sách bảo mật</a></li>
        </ul>
      </li>

      <li class="nav-item auth login">
        <a href="#"><i class="fas fa-sign-in-alt"></i> Đăng nhập</a>
      </li>
      <li class="nav-item auth logout">
        <a href="#"><i class="fas fa-sign-out-alt"></i> Đăng xuất</a>
      </li>
    </ul>
  </nav>
</template>

<script setup>
import { reactive } from 'vue'

const open = reactive({
  product: false,
  docs: false
})

function openMenu(name) {
  open[name] = true
}

function closeMenu(name) {
  open[name] = false
}
</script>

<style scoped>

.navbar {
  display: flex;
  align-items: center;
  background-color: #ffffff;
  padding: 10px 20px;
  box-shadow: 0 2px 8px rgba(0, 0, 0, 0.05);
  position: relative;
  z-index: 100;
}

.nav-logo img {
  height: 40px;
  margin-right: 20px;
}

.nav-links {
  list-style: none;
  display: flex;
  gap: 20px;
  margin: 0;
  padding: 0;
  flex: 1;
}

.nav-item {
  position: relative;
}

.nav-item a {
  text-decoration: none;
  color: #334155;
  font-weight: 500;
  padding: 8px 12px;
  display: inline-block;
  transition: color 0.2s;
}

.nav-item a:hover {
  color: #3b82f6;
}

.dropdown-menu {
  position: absolute;
  top: 100%;
  left: 0;
  background-color: white;
  box-shadow: 0 8px 16px rgba(0,0,0,0.1);
  border-radius: 6px;
  min-width: 180px;
  padding: 8px 0;
  z-index: 10;
}

.dropdown-menu li a {
  display: block;
  padding: 10px 16px;
  color: #64748b;
  font-size: 14px;
  white-space: nowrap;
}

.dropdown-menu li a:hover {
  background-color: #f1f5f9;
  color: #3b82f6;
}

.auth.login a {
  color: #3b82f6;
}
.auth.logout a {
  color: #ef4444;
}
</style>
