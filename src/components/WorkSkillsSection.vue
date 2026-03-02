<script setup lang="ts">
import { ref } from 'vue'
import SectionTitle from '@/components/SectionTitle.vue'

interface SkillItem {
  icon: string
  level: string
  name: string
}

interface SkillCategory {
  title: string
  skills: SkillItem[]
}

const webSkills = ref<SkillCategory>({
  title: '前端技能',
  skills: [
    { name: 'HTML', icon: 'fa-brands fa-html5', level: 'Intermediate' },
    { name: 'CSS', icon: 'fa-brands fa-css3-alt', level: 'Intermediate' },
    { name: 'JavaScript', icon: 'fa-brands fa-square-js', level: 'Intermediate' },
    { name: 'Vue', icon: 'fa-brands fa-vuejs', level: 'Intermediate' },
    { name: 'TypeScript', icon: 'fa-brands fa-typescript', level: 'Basic' },
    { name: 'Tailwind', icon: 'fa-brands fa-tailwind-css', level: 'Intermediate' },
    { name: 'git', icon: 'fa-brands fa-git-alt', level: 'Basic' },
    { name: 'Figma', icon: 'fa-brands fa-figma', level: 'Basic' },
  ],
})
</script>

<template>
  <section class="py-10">
    <div class="text-center font-bold">
      <SectionTitle>
        <template v-slot:chineseTitle>工作技能</template>
        <template v-slot:englishTitle>Skills</template>
      </SectionTitle>

      <div
        class="mt-10 px-5 flex items-center justify-around flex-wrap gap-x-5 gap-y-10 max-w-235 mx-auto"
      >
        <div
          class="icon-div flex items-center justify-center gap-1 transition-transform duration-300 hover:cursor-pointer hover:-translate-y-3 group min-w-42"
          v-for="skill in webSkills.skills"
          :key="skill.name"
        >
          <i
            class="text-5xl"
            :class="{
              [skill.icon]: true, // 一定有 icon class
              'group-hover:text-html': skill.name === 'HTML',
              'group-hover:text-css': skill.name === 'CSS',
              'group-hover:text-js': skill.name === 'JavaScript',
              'group-hover:text-vue': skill.name === 'Vue',
              'group-hover:text-ts': skill.name === 'TypeScript',
              'group-hover:text-tailwind': skill.name === 'Tailwind',
              'group-hover:text-git': skill.name === 'git',
              'bg-burnett-black group-hover:bg-figma bg-clip-text text-transparent':
                skill.name === 'Figma',
            }"
          ></i>
          <div class="text-left">
            <div class="text-xl">{{ skill.name }}</div>
            <div class="text-sm font-light">{{ skill.level }}</div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>
