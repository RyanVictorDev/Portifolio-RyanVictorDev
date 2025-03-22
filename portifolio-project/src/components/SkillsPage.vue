<template>
  <v-container>
    <p class="title mx-auto text-center mb-12 pt-12">Competências</p>
    <v-scode-component class="fade-left" v-if="display.mdAndUp.value" />
    <SkillsCarouselComponent class="reveal" v-else />
  </v-container>
</template>

<script setup lang="ts">
import VScodeComponent from './VScodeComponent.vue';
import SkillsCarouselComponent from './SkillsCarouselComponent.vue';
import { useDisplay } from 'vuetify';

const display = useDisplay();
</script>

<style scoped>

</style>
