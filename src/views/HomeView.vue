<script setup lang="ts">
import MainSection from '@/components/MainSection.vue'
import AboutMeSection from '@/components/AboutMeSection.vue'
import QualificationSection from '@/components/QualificationSection.vue'
import WorkSkillsSection from '@/components/WorkSkillsSection.vue'
import ProjectsSection from '@/components/ProjectsSection.vue'
</script>

<template>
  <div class="max-w-7xl mx-auto p-5">
    <MainSection />
    <AboutMeSection id="about-me" />
    <QualificationSection />
    <WorkSkillsSection id="work-skills" />
    <ProjectsSection id="work-projects" />
  </div>
</template>
