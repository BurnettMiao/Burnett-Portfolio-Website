<script setup lang="ts">
import SectionTitle from '@/components/SectionTitle.vue'
</script>

<template>
  <section class="py-10">
    <div class="text-center font-bold">
      <SectionTitle>
        <template v-slot:chineseTitle>個人資歷</template>
        <template v-slot:englishTitle>Qualification</template>
      </SectionTitle>
    </div>

    <div class="flex items-center justify-center gap-8 mt-10">
      <div class="flex items-center justify-center gap-4">
        <i class="ri-graduation-cap-fill text-3xl"></i>
        <p class="font-bold">Education</p>
      </div>
      <div class="flex items-center justify-center gap-4">
        <i class="ri-briefcase-4-fill text-3xl"></i>
        <p class="font-bold">Experience</p>
      </div>
    </div>

    <div class="mt-1 work-container">
      <div class="work-card">
        <p class="text-xl font-bold">網頁程式設計師</p>
        <p class="work-location">巨匠教育集團</p>
        <div class="work-date">
          <i class="ri-calendar-todo-fill text-2xl"></i>
          <p>2023/12 - 現職</p>
        </div>
      </div>

      <div>
        <div class="work-card-round"></div>
        <div class="work-card-line"></div>
      </div>

      <div></div>
      <div></div>

      <div>
        <div class="work-card-round"></div>
        <div class="work-card-line"></div>
      </div>

      <div>
        <p class="text-xl font-bold">助理工程師</p>
        <p class="work-location">台基寰宇股份有限公司</p>
        <div class="work-date">
          <i class="ri-calendar-todo-fill text-2xl"></i>
          <p>2023/05 - 2023/08</p>
        </div>
      </div>

      <div>
        <p class="text-xl font-bold">專案佐理研究員 / 專責平面及攝影</p>
        <p class="work-location">國家實驗研究院 - 科技政策研究與資訊中心</p>
        <div class="work-date">
          <i class="ri-calendar-todo-fill text-2xl"></i>
          <p>2017/11 - 2022/12</p>
        </div>
      </div>

      <div>
        <div class="work-card-round"></div>
        <div class="work-card-line"></div>
      </div>

      <div></div>
      <div></div>

      <div>
        <div class="work-card-round"></div>
        <div class="work-card-line"></div>
      </div>

      <div>
        <p class="text-xl font-bold">管理師</p>
        <p class="work-location">大千綜合醫院 - 企劃室美編組</p>
        <div class="work-date">
          <i class="ri-calendar-todo-fill text-2xl"></i>
          <p>2016/09 - 2017/09</p>
        </div>
      </div>

      <div>
        <p class="text-xl font-bold">專任教師</p>
        <p class="work-location">育德工家 - 多媒體設計科</p>
        <div class="work-date">
          <i class="ri-calendar-todo-fill text-2xl"></i>
          <p>2015/09 - 2016/07</p>
        </div>
      </div>

      <div>
        <div class="work-card-round"></div>
        <div class="work-card-line"></div>
      </div>

      <div></div>
      <div></div>

      <div>
        <div class="work-card-round"></div>
        <div class="work-card-line"></div>
      </div>

      <div>
        <p class="text-xl font-bold">碩士畢業</p>
        <p class="">國立臺南大學 - 動畫媒體設計研究所</p>
        <div class="work-date">
          <i class="ri-calendar-todo-fill text-2xl"></i>
          <p>2014/07</p>
        </div>
      </div>
    </div>
  </section>
</template>

<style scoped>
.work-container {
  max-width: 575px;
  margin: 2.5rem auto 0 auto;
  display: grid;
  grid-template-columns: 1fr max-content 1fr;
  column-gap: 1.5rem;
}

.work-date {
  margin-top: 0.2rem;
  display: flex;
  align-items: center;
  gap: 0.5rem;
}

.work-card-round {
  display: inline-block;
  width: 13px;
  height: 13px;
  background-color: var(--color-burnett-black);
  border-radius: 50%;
}

.work-card-line {
  display: block;
  width: 1px;
  height: 100%;
  background-color: var(--color-burnett-black);
  transform: translate(6px, -7px);
}

@media (max-width: 640px) {
  .work-container {
    column-gap: 0.6rem;
  }
}
</style>
