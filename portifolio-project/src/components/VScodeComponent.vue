<template>
  <v-container>
    <div class="vsCopy d-flex flex-column rounded-lg">
      <div class="vsHeader rounded-t-lg">
        <div class="d-flex ml-3 ga-2">
          <div class="circle bg-red rounded-circle" />
          <div class="circle bg-yellow rounded-circle" />
          <div class="circle bg-green rounded-circle" />
        </div>
      </div>

      <div class="d-flex flex-row flex-grow-1">
        <div class="vsSidebar d-flex flex-column">
          <v-btn icon="mdi-file-outline" variant="text" />
          <v-btn icon="mdi-github" variant="text" />
          <v-btn icon="mdi-docker" variant="text" />
        </div>

        <div class="vsSecondSidebar d-flex flex-column pa-3">
          <p class="text-white font-weight-bold">Explorer</p>
          <v-expansion-panels class="bg-transparent pa-0 no-shadow" variant="accordion">
            <v-expansion-panel class="bg-transparent no-shadow">
              <v-expansion-panel-title class="text-white">Competências</v-expansion-panel-title>
              <v-expansion-panel-text>
                <v-list class="bg-transparent px-0">
                  <v-list-item v-for="file in files" :key="file.name" class="pa-0" @click="selectedTech = file">
                    <v-list-item-title class="text-body-2 text-white">
                      <v-icon left>{{ file.icon }}</v-icon>
                      {{ file.name }}
                    </v-list-item-title>
                  </v-list-item>
                </v-list>
              </v-expansion-panel-text>
            </v-expansion-panel>
          </v-expansion-panels>
        </div>

        <div v-if="selectedTech" class="tech-description flex-grow-1 pa-4">
          <h3 class="text-white">
            <v-icon left>{{ selectedTech.icon }}</v-icon>
            {{ selectedTech.name }}
          </h3>
          <p class="text-grey-lighten-3 mt-3">{{ selectedTech.description }}</p>
        </div>
      </div>
    </div>
  </v-container>
</template>

<script setup lang="ts">
import { ref } from 'vue';

const files = ref([
  { name: "HTML", icon: "mdi-language-html5", description: "HTML (HyperText Markup Language) é a linguagem de marcação usada para estruturar páginas web." },
  { name: "CSS", icon: "mdi-language-css3", description: "CSS (Cascading Style Sheets) é usado para definir o estilo e layout das páginas web." },
  { name: "JavaScript", icon: "mdi-language-javascript", description: "JavaScript é uma linguagem de programação essencial para tornar páginas web interativas e dinâmicas." },
  { name: "Vue.js", icon: "mdi-vuejs", description: "Vue.js é um framework JavaScript progressivo para a construção de interfaces de usuário reativas." },
  { name: "Quasar", icon: "mdi-vuejs", description: "Quasar Framework é baseado no Vue.js e permite criar aplicações responsivas para múltiplas plataformas." },
  { name: "Java", icon: "mdi-language-java", description: "Java é uma linguagem de programação versátil e amplamente usada no desenvolvimento de software empresarial." },
  { name: "Spring Boot", icon: "mdi-sprout", description: "Spring Boot é um framework que facilita a criação de aplicações Java, reduzindo configurações complexas." },
  { name: "Docker", icon: "mdi-docker", description: "Docker é uma plataforma que permite empacotar aplicações em contêineres para facilitar a implantação e escalabilidade." },
  { name: "Git", icon: "mdi-git", description: "Git é um sistema de controle de versão distribuído, essencial para o desenvolvimento colaborativo de software." },
  { name: "PostgreSQL", icon: "mdi-database", description: "PostgreSQL é um sistema de banco de dados relacional avançado, conhecido por sua robustez e extensibilidade." },
]);

interface Tech {
  name: string;
  icon: string;
  description: string;
}

const selectedTech = ref<Tech | null>(null);
</script>

<style scoped>
.vsCopy {
  display: flex;
  flex-direction: column;
  background-color: #1e1e1e;
  height: 43rem;
  border-radius: 8px;
}

.vsHeader {
  display: flex;
  align-items: center;
  width: 100%;
  height: 3rem;
  background-color: #3c3c3c;
  padding-left: 10px;
}

.circle {
  width: 12px;
  height: 12px;
  margin-right: 5px;
}

.vsSidebar {
  width: 50px;
  background-color: #333;
  display: flex;
  align-items: center;
  padding: 10px 0;
}

.vsSecondSidebar {
  width: 250px;
  background-color: #252526;
}

.no-shadow {
  box-shadow: none !important;
  border: none !important;
}

.tech-description {
  background-color: #2d2d2d;
  color: white;
  border-radius: 5px;
}
</style>
