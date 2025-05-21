<script setup>
import Home from "./components/Home.vue";
import menubar from "./components/menubar.vue";
import minimenu from "./components/minimenu.vue";

import { ref } from 'vue';

const isSidebarOpen = ref(false);
</script>

<template>
    <menubar @toggle="isSidebarOpen = $event" />
    <div :class="['main-container', { 'sidebar-opened': isSidebarOpen }]">
      <minimenu></minimenu>
      <home />
    </div>
</template>

<style scoped>
.main-container {
  position: relative;
  left: 0;
  width: 100%;
  transition: all 0.4s cubic-bezier(0.4, 0, 0.2, 1);
}

.main-container.sidebar-opened {
  left: 250px;
  width: calc(100% - 250px);
}
</style>