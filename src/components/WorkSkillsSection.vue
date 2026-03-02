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
    { name: 'Figma', icon: 'fa-brands fa-square-figma', level: 'Basic' },
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
          class="icon-div flex items-center justify-center gap-1 transition-transform duration-300 hover:cursor-pointer hover:-translate-y-3"
          v-for="skill in webSkills.skills"
          :key="skill.name"
        >
          <i class="text-5xl" :class="skill.icon"></i>
          <div class="text-left">
            <div class="text-xl">{{ skill.name }}</div>
            <div class="text-sm font-light">{{ skill.level }}</div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<style scoped>
.icon-div:hover .fa-html5 {
  color: var(--color-html);
}
.icon-div:hover .fa-css3-alt {
  color: var(--color-css);
}
.icon-div:hover .fa-square-js {
  color: var(--color-js);
}
.icon-div:hover .fa-vuejs {
  color: var(--color-vue);
}
.icon-div:hover .fa-typescript {
  color: var(--color-ts);
}
.icon-div:hover .fa-tailwind-css {
  color: var(--color-tailwind);
}
.icon-div:hover .fa-git-alt {
  color: var(--color-git);
}
.icon-div:hover .fa-square-js {
  color: var(--color-css);
}
</style>
