<template>
  <div class="nav-bar mx-auto rounded-xl border px-6">
    <v-tabs v-if="display.mdAndUp.value" v-model="tabs" slider-color="purple">
      <v-tab
        v-for="item in menuItems"
        :key="item.target"
        class="v-tab text-body-2 pa-0"
        :text="item.text"
        :value="item.target"
        @click="scrollTo(item.target)"
      ></v-tab>
    </v-tabs>

    <v-menu v-else location="bottom center">
      <template v-slot:activator="{ props }">
        <v-btn v-bind="props" class="bg-transparent pa-0 border-none">
          <v-icon>mdi-menu</v-icon>
        </v-btn>
      </template>

      <v-list class="bg-#212121 rounded-lg border text-center justify-center">
        <v-list-item
          v-for="item in menuItems"
          :key="item.text"
          @click="scrollTo(item.target)"
        >
          <v-list-item-title>{{ item.text }}</v-list-item-title>
        </v-list-item>
      </v-list>
    </v-menu>
  </div>
</template>

<script setup lang="ts">
import { ref, onMounted, onUnmounted } from 'vue';
import { useDisplay } from 'vuetify';

const display = useDisplay();
const tabs = ref('home'); 

const menuItems = [
  { text: 'Home', target: 'home' },
  { text: 'Experiências', target: 'experiences' },
  { text: 'Competências', target: 'skills' },
  { text: 'Projetos', target: 'projects' },
  { text: 'Contato', target: 'contact' },
];

const scrollTo = (sectionId: string) => {
  const section = document.getElementById(sectionId);
  if (section) {
    section.scrollIntoView({ behavior: 'smooth', block: 'start' });
  }
};

const updateActiveTab = () => {
  const scrollPosition = window.scrollY;
  let activeSection = 'home';

  menuItems.forEach(({ target }) => {
    const section = document.getElementById(target);
    if (section) {
      const { top } = section.getBoundingClientRect();
      const offsetTop = top + window.scrollY;

      if (scrollPosition >= offsetTop - 150) {
        activeSection = target;
      }
    }
  });

  tabs.value = activeSection;
};

onMounted(() => {
  window.addEventListener('scroll', updateActiveTab);
  updateActiveTab();
});

onUnmounted(() => {
  window.removeEventListener('scroll', updateActiveTab);
});
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
