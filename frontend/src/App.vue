<script setup>
import AppHeader from './components/AppHeader.vue'
import HeroSection from './components/HeroSection.vue'
import ProjectsSection from './components/ProjectsSection.vue'
import SkillsSection from './components/SkillsSection.vue'
import ContactSection from './components/ContactSection.vue'
import AppFooter from './components/AppFooter.vue'
</script>

<template>
  <a class="skip-link" href="#main-content"> Skip to content </a>

  <AppHeader />

  <main id="main-content" tabindex="-1">
    <HeroSection />
    <ProjectsSection />
    <SkillsSection />
    <ContactSection />
  </main>

  <AppFooter />
</template>
