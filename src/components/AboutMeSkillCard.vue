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
  <div
    v-for="skill in skillArr"
    :key="skill.icon"
    class="p-4 rounded-2xl flex flex-col items-center justify-center border border-burnett-black cursor-pointer w-33.75"
  >
    <i class="text-3xl mb-2" :class="skill.icon"></i>
    <div>{{ skill.title }}</div>
    <div>{{ skill.text }}</div>
  </div>
</template>
