<template>
  <v-app class="bg-black fill-height">
    <NavBar />
    <HomePage class="mb-12" />
    <ExperiencesPage class="mb-12" />
    <SkillsPage />
  </v-app>
</template>

<script lang="ts" setup>
import ExperiencesPage from '@/components/ExperiencesPage.vue';
import HomePage from '@/components/HomePage.vue';
import NavBar from '@/components/NavBar.vue';
import SkillsPage from '@/components/SkillsPage.vue';

</script>
