<script setup lang="ts">
import { ref } from 'vue'

interface FileLinkType {
  icon: string
  link: string
}

const fileLinksArr = ref<FileLinkType[]>([
  {
    icon: 'ri-github-fill',
    link: 'https://github.com/BurnettMiao',
  },
  {
    icon: 'ri-linkedin-box-fill',
    link: 'https://www.linkedin.com/in/burnett-miao-94609a98/',
  },
  {
    icon: 'ri-file-list-3-fill',
    link: 'https://burnettmiao.github.io/Digital-Resume/',
  },
])
</script>
<template>
  <div class="border-t border-burnett-black">
    <div class="max-w-7xl mx-auto px-5 py-7 flex items-center justify-between">
      <div class="text-[22px] font-bold">Burnett's portfolio</div>

      <!-- icon 區域 -->
      <div class="flex gap-8">
        <a v-for="(file, index) in fileLinksArr" :key="index" :href="file.link" target="_blank">
          <i class="text-3xl" :class="file.icon"></i>
        </a>
      </div>
    </div>
  </div>
</template>
