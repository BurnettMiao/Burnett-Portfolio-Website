<script setup lang="ts">
import { ref } from 'vue'

interface DesignProjectsItem {
  img: string
  title: string
}

const props = defineProps<{ designProjects: DesignProjectsItem[] }>()
const currentImg = ref<null | string>(null)

const showDesignImg = ref<boolean>(false)
function openDesignImg(imgSrc: string) {
  showDesignImg.value = true
  currentImg.value = imgSrc
}

function closeDesignImg() {
  showDesignImg.value = false
  currentImg.value = null
}
</script>

<template>
  <div class="mt-8">
    <div class="flex flex-wrap items-center justify-center gap-8">
      <div
        @click="openDesignImg(poster.img)"
        v-for="poster in props.designProjects"
        :key="poster.title"
        class="border border-gray-300 rounded-xl overflow-hidden cursor-pointer hover:shadow-md relative group"
      >
        <div class="max-w-60 cursor-pointer">
          <img :src="poster.img" alt="" loading="lazy" />
        </div>
      </div>
    </div>
  </div>

  <div
    @click="closeDesignImg"
    v-if="showDesignImg"
    class="bg-gray-300/30 backdrop-blur-sm fixed inset-0 z-20 flex items-center justify-center"
  >
    <div
      class="h-auto max-h-[90%] sm:h-[90%] w-auto max-w-[90%] sm:max-w-275 flex items-center justify-center relative"
    >
      <img
        v-if="currentImg"
        class="h-full w-auto max-w-full object-contain"
        :src="currentImg"
        alt=""
      />

      <div
        @click="closeDesignImg"
        class="absolute top-3 right-3 bg-white shadow-sm w-8 h-8 rounded-full flex items-center justify-center cursor-pointer group"
      >
        <i
          class="fa-solid fa-xmark rotate-0 duration-300 transition-transform ease-in-out group-hover:rotate-90"
        ></i>
      </div>
    </div>
  </div>
</template>
