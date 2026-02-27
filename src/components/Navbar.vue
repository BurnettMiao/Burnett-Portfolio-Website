<script setup lang="ts">
import { ref } from 'vue'

const navItems = ref<string[]>(['關於我', '工作技能', '作品集'])
const isOpen = ref<boolean>(false)

function toggleOpen() {
  isOpen.value = !isOpen.value
}
</script>

<template>
  <div class="w-full p-5 bg-amber-300 border-b border-gray-300 shadow-sm">
    <div class="max-w-7xl mx-auto flex items-center justify-between">
      <div class="text-[22px] font-bold">Burnett's portfolio</div>

      <div class="hidden sm:flex items-center gap-5">
        <div class="relative nav-item hover:cursor-pointer" v-for="item in navItems" :key="item">
          {{ item }}
        </div>
      </div>

      <i
        v-if="isOpen"
        @click="toggleOpen"
        class="ri-menu-line cursor-pointer text-2xl sm:hidden"
      ></i>

      <i
        v-else
        @click="toggleOpen"
        class="ri-close-large-line cursor-pointer text-2xl sm:hidden"
      ></i>
    </div>
  </div>
</template>

<style scoped>
.nav-item::after {
  content: '';
  position: absolute;
  bottom: -3px;
  left: 0px;
  width: 100%;
  height: 1px;
  transform: scaleX(0);
  transform-origin: right center;
  background-color: black;
  transition: transform 0.6s cubic-bezier(0.19, 1, 0.022, 1);
}

.nav-item:hover::after {
  transform: scaleX(1);
  transform-origin: left center;
}
</style>
