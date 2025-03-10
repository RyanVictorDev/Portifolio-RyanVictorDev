<template>
  <v-app class="bg-black fill-height">
    <NavBar />
    <HomePage />
    <ExperiencesPage />
  </v-app>
</template>

<script lang="ts" setup>
import ExperiencesPage from '@/components/ExperiencesPage.vue';
import HomePage from '@/components/HomePage.vue';
import NavBar from '@/components/NavBar.vue';
</script>
