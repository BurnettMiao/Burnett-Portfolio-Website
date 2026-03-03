<script setup lang="ts">
import { ref } from 'vue'

const props = defineProps<{ photographs: string[] }>()

const currentImg = ref<null | string>(null)

const showDesignImg = ref<boolean>(false)

const showImgItem = ref<number>(8)

function addShowImgItem() {
  if (showImgItem.value < props.photographs.length) {
    showImgItem.value += 4
    return
  }

  return
}

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
        @click="openDesignImg(poster)"
        v-for="poster in props.photographs.slice(0, showImgItem)"
        :key="poster"
        class="border border-gray-300 rounded-xl overflow-hidden cursor-pointer hover:shadow-md relative group"
      >
        <div class="max-w-60 cursor-pointer">
          <img :src="poster" alt="" loading="lazy" />
        </div>
      </div>
    </div>

    <div class="flex items-center justify-center mt-10">
      <div
        v-if="showImgItem < props.photographs.length"
        @click="addShowImgItem"
        class="px-5 py-3 rounded-xl bg-amber-300 cursor-pointer"
      >
        SHOW MORE
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
