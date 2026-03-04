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

    <div class="flex flex-col items-center justify-around gap-8 mt-10 md:flex-row">
      <div class="w-full md:w-1/3 flex items-center justify-center">
        <img class="w-70 rounded-2xl" src="../assets/images/Miao-1.jpeg" alt="" />
      </div>

      <div class="w-full md:w-2/3 px-2 sm:p-4">
        <div>
          <div>
            畢業於國立臺南大學動畫媒體設計研究所，具設計與動畫背景，對視覺呈現與使用者體驗具敏感度。現職負責企業內部教育訓練與學習紀錄平台之前端開發，使用
            Vue 進行元件化設計，並透過 Side Project 持續深化實作能力。
          </div>

          <div class="mt-2">
            熟悉 Tailwind CSS，具備獨立切版與響應式開發經驗；亦使用 Figma 進行設計溝通與 UI/UX
            討論。熱愛登山與攝影，將設計觀察力融入前端開發之中。作品可參閱 GitHub。
          </div>
        </div>

        <AboutMeSkillCard :skillArr="skillArr" />
      </div>
    </div>
  </section>
</template>
