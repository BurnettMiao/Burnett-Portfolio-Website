<script setup lang="ts">
import AboutMeSkillCard from '@/components/AboutMeSkillCard.vue'
import SectionTitle from '@/components/SectionTitle.vue'

interface Skill {
  icon: string
  title: string
  text: string
}

const skillArr: Skill[] = [
  {
    icon: 'ri-window-fill',
    title: '網頁設計',
    text: '10+ Projects',
  },
  {
    icon: 'ri-folder-image-fill',
    title: '平面設計',
    text: '5+ Years',
  },
  {
    icon: 'ri-film-fill',
    title: '影片剪輯',
    text: '5+ Years',
  },
  {
    icon: 'ri-camera-3-fill',
    title: '活動攝影',
    text: '5+ Years',
  },
]
</script>

<template>
  <section class="py-10">
    <div class="text-center font-bold">
      <SectionTitle>
        <template v-slot:chineseTitle>關於我</template>
        <template v-slot:englishTitle>About Me</template>
      </SectionTitle>
    </div>

    <div class="flex flex-col items-center justify-around gap-8 mt-2 md:flex-row">
      <div class="w-full md:w-1/3 flex items-center justify-center">
        <img class="w-70 rounded-2xl" src="../assets/images/Miao-1.jpeg" alt="" />
      </div>

      <div class="w-full md:w-2/3 px-2 sm:p-4">
        <div>
          <div>
            個人畢業於國立臺南大學動畫媒體設計研究所，具備設計與動畫製作背景，對於視覺呈現與使用者體驗具備良好敏感度。現職負責集團內部教育訓練影片播放平台與學習紀錄系統之前端開發與維護，並支援內外部專案網站製作。專案中以
            Vue 作為核心開發框架，透過元件化設計提升可維護性與重用性，並持續以 Side Project 深化對
            Vue 生態系的理解與實作能力。
          </div>
          <div class="mt-4">
            在樣式管理方面，熟悉 Tailwind CSS 與
            Bootstrap，具備獨立切版與響應式頁面製作經驗；亦於專案初期使用 Figma
            製作設計稿並與需求單位進行 UI/UX
            討論，確保版面資訊傳達清晰且貼近使用情境。平時喜愛登山與攝影，培養對構圖與細節的觀察力，並將設計思維融入前端開發之中。相關作品可參閱
            GitHub。
          </div>
        </div>

        <div class="flex flex-wrap items-center justify-around gap-4 mt-6">
          <AboutMeSkillCard :skillArr="skillArr" />
        </div>
      </div>
    </div>
  </section>
</template>
