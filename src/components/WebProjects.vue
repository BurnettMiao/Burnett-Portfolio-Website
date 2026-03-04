<script setup lang="ts">
import { ref } from 'vue'

interface WebProjectsItem {
  img: string
  title: string
  link: string
}

const props = defineProps<{ webProjects: WebProjectsItem[] }>()

const showWebItem = ref<number>(8)

function addShowWebItem() {
  if (showWebItem.value < props.webProjects.length) {
    showWebItem.value += 4
    return
  }

  return
}
</script>

<template>
  <div class="mt-8">
    <div class="flex flex-wrap items-center justify-center gap-8">
      <a
        :href="web.link"
        target="_blank"
        class="flex flex-col items-center justify-center gap-2 border border-gray-300 rounded-xl overflow-hidden cursor-pointer hover:shadow-md relative group"
        v-for="web in webProjects.slice(0, showWebItem)"
        :key="web.title"
      >
        <div class="max-w-60">
          <img class="w-full" :src="web.img" alt="" />
        </div>
        <div
          class="max-w-60 w-full px-3 pt-1 pb-3 absolute inset-x-0 bottom-0 bg-white/50 backdrop-blur-sm translate-y-full group-hover:translate-y-0 transition-transform duration-300 ease-in-out rounded-t-sm flex"
        >
          <div class="line-clamp-1 font-bold flex-1 text-outline">
            {{ web.title }}
          </div>
          <div class="text-burnett-blue">
            <i class="fa-solid fa-up-right-from-square"></i>
          </div>
        </div>
      </a>
    </div>
    <div class="flex items-center justify-center mt-10">
      <div
        v-if="showWebItem < webProjects.length"
        @click="addShowWebItem"
        class="px-5 py-3 rounded-xl bg-burnett-blue text-white cursor-pointer shadow-lg hover:shadow-none transition-all duration-200 ease-in-out hover:-translate-y-1"
      >
        SHOW MORE
      </div>
    </div>
  </div>
</template>

<style scoped></style>
