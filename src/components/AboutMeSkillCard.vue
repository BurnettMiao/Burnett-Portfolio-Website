<script setup lang="ts">
interface Skill {
  icon: string
  title: string
  text: string
}

const prop = defineProps<{
  skillArr: Skill[]
}>()
</script>

<template>
  <div class="flex flex-wrap items-center justify-center mt-6">
    <template v-for="(skill, index) in skillArr" :key="skill.icon">
      <!-- 每個技能項目 -->
      <div class="flex flex-col items-center justify-center cursor-pointer w-33.75 p-3">
        <i class="text-3xl mb-2" :class="skill.icon"></i>
        <div>{{ skill.title }}</div>
        <div class="text-sm text-gray-600">{{ skill.text }}</div>
      </div>

      <!-- 分隔線：除了最後一個項目外都顯示 -->
      <div
        v-if="index < skillArr.length - 1"
        class="w-px h-10 bg-burnett-black mx-2 self-center"
      ></div>
    </template>
  </div>
</template>
