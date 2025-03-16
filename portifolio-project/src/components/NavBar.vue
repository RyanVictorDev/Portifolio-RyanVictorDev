<template>
  <div class="nav-bar mx-auto rounded-xl border px-6">
    <v-tabs v-model="tabs" slider-color="purple">
      <v-tab class="v-tab text-body-2 pa-0" text="Home" @click="scrollTo('home')"></v-tab>
      <v-tab class="v-tab text-body-2" text="Experiências" @click="scrollTo('experiences')"></v-tab>
      <v-tab class="v-tab text-body-2" text="Competências" @click="scrollTo('skills')"></v-tab>
      <v-tab class="v-tab text-body-2" text="Projetos" @click="scrollTo('projects')"></v-tab>
      <v-tab class="v-tab text-body-2" text="Contato" @click="scrollTo('contact')"></v-tab>
    </v-tabs>
  </div>
</template>

<script lang="ts" setup>
import { ref } from 'vue';

const tabs = ref(null);

const scrollTo = (sectionId: string) => {
  const section = document.getElementById(sectionId);
  if (section) {
    section.scrollIntoView({ behavior: 'smooth', block: 'start' });
  }
};
</script>

<style scoped>
.nav-bar {
  display: flex;
  max-width: 45%;
  padding: 0.1rem;
  background-color: #2b2b2b6e;
  position: fixed;
  z-index: 100;
  left: 50%;
  top: 1rem;
  transform: translateX(-50%);
}

.v-tab {
  padding: 4px 8px !important;
  min-width: auto !important;
}
</style>
