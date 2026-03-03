<script setup lang="ts">
import { ref } from 'vue'
import SectionTitle from '@/components/SectionTitle.vue'

interface SkillItem {
  icon: string
  level: number
  name: string
}

interface SkillCategory {
  title: string
  skills: SkillItem[]
}

const webSkills = ref<SkillCategory>({
  title: '前端技能',
  skills: [
    { name: 'HTML', icon: 'fa-brands fa-html5', level: 4 },
    { name: 'CSS', icon: 'fa-brands fa-css3-alt', level: 4 },
    { name: 'JavaScript', icon: 'fa-brands fa-square-js', level: 4 },
    { name: 'Vue', icon: 'fa-brands fa-vuejs', level: 4 },
    { name: 'TypeScript', icon: 'fa-brands fa-typescript', level: 3 },
    { name: 'Tailwind', icon: 'fa-brands fa-tailwind-css', level: 4 },
    { name: 'git', icon: 'fa-brands fa-git-alt', level: 3 },
    { name: 'Figma', icon: 'fa-brands fa-figma', level: 3 },
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
        class="mt-10 px-0 sm:px-5 flex items-center justify-around flex-wrap gap-x-5 gap-y-10 max-w-235 mx-auto"
      >
        <div
          class="icon-div flex items-center justify-center gap-1 transition-transform duration-300 hover:cursor-pointer hover:-translate-y-3 group"
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
            <div>
              <i
                v-for="n in 5"
                :key="n"
                class="group-hover:text-amber-300 text-[12px]"
                :class="n <= skill.level ? 'fa-solid fa-star' : 'fa-regular fa-star'"
              ></i>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>
