<script setup lang="ts">
import { ref } from 'vue'

interface NavItem {
  label: string
  id: string
}

const navItems = ref<NavItem[]>([
  { label: '關於我', id: 'about-me' },
  { label: '工作技能', id: 'work-skills' },
  { label: '作品集', id: 'work-projects' },
])
const isOpen = ref<boolean>(false)

function toggleOpen() {
  isOpen.value = !isOpen.value
}

function scrollToSection(id: string) {
  const element = document.getElementById(id)

  if (element) {
    const navbarHeight = 70
    const y = element.getBoundingClientRect().top + window.scrollY - navbarHeight
    window.scrollTo({ top: y, behavior: 'smooth' })
  }
}
</script>

<template>
  <div class="w-full p-5 border-b border-gray-300 shadow-sm fixed top-0 left-0 bg-burnett-bg z-50">
    <div class="max-w-7xl mx-auto flex items-center justify-between">
      <div class="text-[22px] font-bold">Burnett's portfolio</div>

      <div class="hidden sm:flex items-center gap-5">
        <div
          @click="scrollToSection(item.id)"
          class="relative nav-item hover:cursor-pointer"
          v-for="item in navItems"
          :key="item.id"
        >
          {{ item.label }}
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
