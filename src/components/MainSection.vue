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

const cv: string =
  'https://docs.google.com/document/d/1qbcKyAgez-Nh6bHPtWTPscqEG5JIeXz-YI0F6XWLDM8/edit?tab=t.0'
</script>

<template>
  <section class="flex flex-col md:flex-row items-center justify-around gap-8 mt-2 pb-10 sm:mt-6">
    <!-- 左半部 -->
    <div class="flex items-center gap-5 md:w-1/2 order-2 md:order-1">
      <!-- icon 區域 -->
      <div class="flex flex-col gap-2">
        <a v-for="(file, index) in fileLinksArr" :key="index" :href="file.link" target="_blank">
          <i class="text-2xl" :class="file.icon"></i>
        </a>
      </div>
      <!-- 自我介紹區域 -->
      <div class="flex flex-col gap-4 items-start">
        <div>
          <div>
            <span class="text-3xl sm:text-[36px] font-bold">繆照慶</span>
            <span class="text-xl sm:text-2xl ml-3">Burnett Miao</span>
          </div>

          <div class="flex items-center gap-2">
            <div class="w-12.5 h-px bg-burnett-black"></div>
            <div>前端網頁工程師</div>
          </div>
        </div>

        <div>
          因工作需求誤打誤撞意外發現對於前端網頁有興趣的奇怪人物，想用網頁傳達出非平面設計所能營造出的另一種視覺互動感受之體驗
        </div>

        <div
          class="inline-block px-4 py-2 border border-burnett-black bg-burnett-black text-white rounded-lg cursor-pointer hover:bg-white hover:text-burnett-black transition-colors ease duration-300"
        >
          Download CV
        </div>
      </div>
    </div>

    <!-- 右半部 -->
    <div class="main-img sm:w-1/2 order-1 md:order-2"></div>
  </section>
</template>

<style scoped>
.main-img {
  background: url(../assets/images/Miao-1.jpeg);
  background-repeat: no-repeat;
  background-position: center;
  background-size: cover;
  aspect-ratio: 1/1;
  width: 380px;
  height: 380px;
  box-shadow: inset 0 0 0 9px rgb(225 225 225 / 30%);
  order: 1;
  justify-self: center;
  animation: profile_animate 8s ease-in-out infinite 1s;
}

@keyframes profile_animate {
  0% {
    border-radius: 60% 40% 30% 70%/60% 30% 70% 40%;
  }

  50% {
    border-radius: 30% 60% 70% 40%/50% 60% 30% 60%;
  }

  100% {
    border-radius: 60% 40% 30% 70%/60% 30% 70% 40%;
  }
}

@media (max-width: 640px) {
  .main-img {
    width: 250px;
    height: 250px;
  }
}
</style>
