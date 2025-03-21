<template>
  <v-app class="bg-black">
    <NavBar />
    <HomePage id="home" class="mb-12" />
    <ExperiencesPage id="experiences" class="mb-12 pt-12" />
    <SkillsPage id="skills" class="mb-12 pt-12" />
    <ProjectsPage id="projects" class="mb-12 pt-12" />
    <ContactPage id="contact" class="mb-12 pt-12" />
  </v-app>
</template>

<script lang="ts" setup>
import ContactPage from '@/components/ContactPage.vue';
import ExperiencesPage from '@/components/ExperiencesPage.vue';
import HomePage from '@/components/HomePage.vue';
import NavBar from '@/components/NavBar.vue';
import ProjectsPage from '@/components/ProjectsPage.vue';
import SkillsPage from '@/components/SkillsPage.vue';

import ScrollReveal from "scrollreveal";
import { onMounted } from 'vue';

onMounted(() => {
  ScrollReveal().reveal(".reveal", {
    duration: 1000,
    origin: "bottom",
    distance: "50px",
    delay: 200,
    reset: true,
  });

  ScrollReveal().reveal(".fade-left", {
    duration: 1200,
    origin: "left",
    distance: "100px",
    delay: 300,
    reset: true,
  });

  ScrollReveal().reveal(".fade-right", {
    duration: 1200,
    origin: "right",
    distance: "100px",
    delay: 300,
    reset: true,
  });
});

</script>
