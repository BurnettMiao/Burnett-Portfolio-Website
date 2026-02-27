<script setup lang="ts">
import SectionTitle from '@/components/SectionTitle.vue'
</script>

<template>
  <section class="py-10">
    <div class="text-center font-bold">
      <SectionTitle>
        <template v-slot:chineseTitle>工作技能</template>
        <template v-slot:englishTitle>Skills</template>
      </SectionTitle>
    </div>
  </section>
</template>
