<script setup lang="ts">
import { ref } from 'vue'
import SectionTitle from '@/components/SectionTitle.vue'

// 網頁圖片縮圖
import ASimpleResponsiveLandingPage from '@/assets/images/web/20231108/A-Simple-Responsive-Landing-Page.jpg'
import TailwindManageLandingPage from '@/assets/images/web/20231108/Tailwind-manage-landing-page.jpg'
import MovieAppCoding from '@/assets/images/web/20231108/Movie-App-Coding_Practice.jpg'
import ImageSearchApp from '@/assets/images/web/20231108/Image-Search-App.jpg'
import AnimatedLoginPage from '@/assets/images/web/20231108/Animated-Login-Page.jpg'
import MinimalWeatherAppUiDesign from '@/assets/images/web/20231108/Minimal-Weather-App-Ui-Design_Practice.jpg'
import WeatherAppWithJavascript from '@/assets/images/web/20231108/Weather-App-With-Javascript_Practice.jpg'
import CompleteResponsivePortfolioDesign from '@/assets/images/web/20231108/Complete-Responsive-Portfolio-Design_Practice.jpg'
import EngagingTravelAgencyWebsiteLandingPage from '@/assets/images/web/20231108/Designing-an-Engaging-Travel-Agency-Website-Landing-Page.jpg'
import InteriorECommerceWebsite from '@/assets/images/web/20231108/Design-an-Interior-E-Commerce-Website_Practice.jpg'
import VueMonsterSlayerProject from '@/assets/images/web/20231108/Vue-MonsterSlayerProject-Practice.jpg'
import TravelWebsiteLandingPage from '@/assets/images/web/20231108/Design-a-Travel-Website-Landing-Page_Practice.jpg'
import EstateResponsiveLandingPage from '@/assets/images/web/20231108/A-Real-Estate-Responsive-Landing-Page.jpg'
import ApexChartsPage from '@/assets/images/web/20230417/apex-charts_Practice.jpg'
import StarbucksLandingPage from '@/assets/images/web/20230417/Build-a-Starbucks-Landing-Page-Clone.jpg'
import CalculatorPage from '@/assets/images/web/20230417/Calculator_Practice.jpg'
import MusicPlayerPage from '@/assets/images/web/20230417/music-player_Practice.jpg'
import SunnysideLandingPage from '@/assets/images/web/20230417/Sunnyside-Landing-Page_Practice.jpg'
import UnifeedBlogTemplateStarterPage from '@/assets/images/web/20230417/Unifeed-Blog-Template-Starter-Files.jpg'
import ChatTalkerAI from '@/assets/images/web/first/ChatTalkerAI.jpg'
import ClipboardLandingPage from '@/assets/images/web/first/clipboard-landing-page-master.jpg'
import FiberStarterFilesPage from '@/assets/images/web/first/Fiber-Starter-Files.jpg'
import NewsHomepage from '@/assets/images/web/first/news-homepage-main.jpg'
import YSF from '@/assets/images/web/first/YSFxWorld.jpg'
import YSFOfficePage from '@/assets/images/web/first/YSF.jpg'

interface LabelItem {
  icon: string
  title: string
}

const labels = ref<LabelItem[]>([
  { icon: 'fa-regular fa-window-restore', title: 'Web' },
  { icon: 'fa-solid fa-object-group', title: 'Design' },
  { icon: 'fa-solid fa-images', title: 'Photograph' },
])

const webProjects = ref([
  {
    img: ASimpleResponsiveLandingPage,
    title: 'A Simple Responsive Landing Page',
    link: 'https://burnettmiao.github.io/A-Simple-Responsive-Landing-Page/',
  },
  {
    img: TailwindManageLandingPage,
    title: 'Tailwind Manage Landing Page',
    link: 'https://burnettmiao.github.io/Tailwind-manage-landing-page/',
  },
  {
    img: MovieAppCoding,
    title: 'Movie App Coding',
    link: 'https://burnettmiao.github.io/Movie-App-Coding_Practice/',
  },
  {
    img: ImageSearchApp,
    title: 'Image Search App',
    link: 'https://burnettmiao.github.io/Image-Search-App/',
  },
  {
    img: AnimatedLoginPage,
    title: 'Animated Login Page',
    link: 'https://burnettmiao.github.io/Animated-Login-Page/',
  },
  {
    img: MinimalWeatherAppUiDesign,
    title: 'Minimal Weather App Ui Design',
    link: 'https://burnettmiao.github.io/Minimal-Weather-App-Ui-Design_Practice/',
  },
  {
    img: WeatherAppWithJavascript,
    title: 'Weather App With Javascript',
    link: 'https://burnettmiao.github.io/Weather-App-With-Javascript_Practice/',
  },
  {
    img: CompleteResponsivePortfolioDesign,
    title: 'Complete Responsive Portfolio Design',
    link: 'https://burnettmiao.github.io/Complete-Responsive-Portfolio-Design_Practice/',
  },
  {
    img: EngagingTravelAgencyWebsiteLandingPage,
    title: 'Engaging Travel Agency Website Landing Page',
    link: 'https://burnettmiao.github.io/Designing-an-Engaging-Travel-Agency-Website-Landing-Page/',
  },
  {
    img: InteriorECommerceWebsite,
    title: 'Interior E-Commerce Website',
    link: 'https://burnettmiao.github.io/Design-an-Interior-E-Commerce-Website_Practice/',
  },
  {
    img: VueMonsterSlayerProject,
    title: 'Vue Monster Slayer Project',
    link: 'https://burnettmiao.github.io/Vue-MonsterSlayerProject-Practice/',
  },
  {
    img: TravelWebsiteLandingPage,
    title: 'Travel Website Landing Page',
    link: 'https://burnettmiao.github.io/Design-a-Travel-Website-Landing-Page_Practice/',
  },
  {
    img: EstateResponsiveLandingPage,
    title: 'Estate Responsive Landing Page',
    link: 'https://burnettmiao.github.io/A-Real-Estate-Responsive-Landing-Page/',
  },
  {
    img: ApexChartsPage,
    title: 'Apex Charts Page',
    link: 'https://burnettmiao.github.io/apex-charts_Practice/',
  },
  {
    img: StarbucksLandingPage,
    title: 'Starbucks Landing Page',
    link: 'https://burnettmiao.github.io/Build-a-Starbucks-Landing-Page-Clone_Practice/',
  },
  {
    img: CalculatorPage,
    title: 'Calculator Page',
    link: 'https://burnettmiao.github.io/Calculator_Practice/',
  },
  {
    img: MusicPlayerPage,
    title: 'Music Player Page',
    link: 'https://burnettmiao.github.io/music-player_Practice/',
  },
  {
    img: SunnysideLandingPage,
    title: 'Sunnyside Landing Page',
    link: 'https://burnettmiao.github.io/Sunnyside-Landing-Page_Practice/',
  },
  {
    img: UnifeedBlogTemplateStarterPage,
    title: 'Unifeed Blog Template Starter Page',
    link: 'https://burnettmiao.github.io/Unifeed-Blog-Template-Starter-Files_Practice/',
  },
  {
    img: ChatTalkerAI,
    title: '六角學院ChatTalkerAI網頁',
    link: 'https://burnettmiao.github.io/ChatTalkerAI_Practice/',
  },
  {
    img: ClipboardLandingPage,
    title: 'Clipboard Landing Page',
    link: 'https://burnettmiao.github.io/clipboard-landing-page-master_Practice/',
  },
  {
    img: FiberStarterFilesPage,
    title: 'Fiber Starter Files Page',
    link: 'https://burnettmiao.github.io/Fiber-Starter-Files_Practice/',
  },
  {
    img: NewsHomepage,
    title: 'News Homepage',
    link: 'https://burnettmiao.github.io/news-homepage-main_Practice/',
  },
  // 已失效
  // {
  //   img: YSFOfficePage,
  //   title: 'YSF 首頁版面更新',
  //   link: 'https://ysgrant.stpi.narl.org.tw/index.php',
  // },
  // 已失效
  // {
  //   img: YSF,
  //   title: 'YSF 成果展現網頁',
  //   link: '',
  // },
])

const currentLabel = ref<string>('Web')
const showWebItem = ref<number>(8)

function changeCurrentLabel(label: string) {
  currentLabel.value = label
}

function addShowWebItem() {
  if (showWebItem.value < webProjects.value.length) {
    showWebItem.value += 4
    return
  }

  return
}
</script>

<template>
  <section class="py-10">
    <div class="text-center font-bold">
      <SectionTitle>
        <template v-slot:chineseTitle>作品集</template>
        <template v-slot:englishTitle>Projects</template>
      </SectionTitle>
    </div>

    <!-- 上方 label 按鈕 -->
    <div class="flex items-center justify-center mt-10 gap-10">
      <div
        v-for="label in labels"
        :key="label.title"
        class="flex flex-wrap gap-2 items-center cursor-pointer label-item relative pb-1"
        :class="{ active: label.title === currentLabel }"
        @click="changeCurrentLabel(label.title)"
      >
        <i :class="label.icon" class="text-2xl"></i>
        <span class="text-xl">{{ label.title }}</span>
      </div>
    </div>

    <!-- 下方切換對應頁面 -->
    <!-- Web -->
    <div class="mt-8">
      <div class="flex flex-wrap items-center justify-center gap-8">
        <div
          class="flex flex-col items-center justify-center gap-2 border border-gray-300 rounded-xl overflow-hidden cursor-pointer hover:shadow-md relative group"
          v-for="web in webProjects.slice(0, showWebItem)"
          :key="web.title"
        >
          <div class="max-w-60">
            <img class="w-full" :src="web.img" alt="" />
          </div>
          <div
            class="max-w-60 w-full px-3 pt-1 pb-3 absolute inset-x-0 bottom-0 bg-white/10 backdrop-blur-sm translate-y-full group-hover:translate-y-0 transition-transform duration-300 ease-in-out rounded-t-xl"
          >
            <div class="line-clamp-1 font-bold">
              {{ web.title }}
            </div>
            <a :href="web.link" target="_blank" class="text-amber-300">
              View Page <i class="fa-solid fa-up-right-from-square"></i>
            </a>
          </div>
        </div>
      </div>
      <div class="flex items-center justify-center mt-10">
        <div
          v-if="showWebItem < webProjects.length"
          @click="addShowWebItem"
          class="px-5 py-3 rounded-xl bg-amber-300 cursor-pointer"
        >
          SHOW MORE
        </div>
      </div>
    </div>
  </section>
</template>

<style scoped>
.label-item::after {
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

.label-item:hover::after {
  transform: scaleX(1);
  transform-origin: left center;
}

.label-item.active::after {
  content: '';
  position: absolute;
  bottom: -3px;
  left: 0px;
  width: 100%;
  height: 1px;
  transform: scaleX(1);
  background-color: black;
}
</style>
