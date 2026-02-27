<script setup lang="ts">
import AboutMeSkillCard from '@/components/AboutMeSkillCard.vue'

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
      <span class="text-3xl">關於我</span> <span class="text-2xl ml-3">About Me</span>
    </div>

    <div class="flex flex-col items-center justify-around gap-8 mt-2 md:flex-row">
      <div class="w-full md:w-1/3 flex items-center justify-center">
        <img class="w-70 rounded-2xl" src="../assets/images/Miao-1.jpeg" alt="" />
      </div>

      <div class="w-full md:w-2/3 p-4">
        <div>
          個人畢業於國立臺南大學動畫媒體設計研究所，平時喜愛爬山踏青接近大自然，對於攝影也有所涉獵。我擁有設計與動畫的技術背景，目前臺灣大多公司多以Vue來開發專案，因此我在前端三大框架中也選擇Vue來作為學習目標，目前常應用前端框架Vue，並使用Vue建立自己的Side
          Project，從實作中建立起對Vue的深入瞭解。我對於Tailwind CSS也有所著墨，具有使用Tailwind
          CSS與Bootstrap實作切版網頁的相關經驗，亦有獨立網頁切版的能力。我採用Figma製作設計稿與使用者溝通，相關網頁作品請參閱我的GitHub網站。
        </div>

        <div class="flex flex-wrap items-center justify-around gap-4 mt-6">
          <AboutMeSkillCard :skillArr="skillArr" />
        </div>
      </div>
    </div>
  </section>
</template>
