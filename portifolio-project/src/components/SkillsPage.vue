<template>
  <v-container>
    <p class="title mx-auto text-center mb-12 pt-12">Competências</p>

    <div class="vsCopy d-flex flex-column rounded-lg">
      <div class="vsHeader rounded-t-lg">
        <div class="d-flex ml-3 mr-auto ga-1">
          <div class="circle bg-red rounded-circle" />
          <div class="circle bg-yellow rounded-circle" />
          <div class="circle bg-green rounded-circle" />
        </div>
        <!-- <p class="align-center mx-auto position-absolute">Front-end</p> -->
      </div>

      <div class="d-flex flex-row">
        <div class="d-flex flex-column rounded-bs-lg ga-2 vsSidebar">
          <v-btn class="mx-auto" icon="$vuetify" variant="text" />
          <v-btn class="mx-auto" icon="$vuetify" variant="text" />
          <v-btn class="mx-auto" icon="$vuetify" variant="text" />
        </div>

        <div class="d-flex flex-column vsSecondSidebar">
          <p class="align-left pl-6 mt-2">Explorer</p>

          <v-expansion-panels class="bg-transparent pa-0 no-shadow" variant="accordion">
            <v-expansion-panel class="bg-transparent no-shadow">
              <v-expansion-panel-title>Competências</v-expansion-panel-title>
              <v-expansion-panel-text class="">
                <v-list class="bg-transparent px-0">
                  <v-list-item
                    v-for="file in files"
                    :key="file.name"
                    class="pa-0"
                    @click="selectedTech = file"
                  >
                    <v-btn class="full-btn bg-transparent border-0">
                      <v-list-item-title>{{ file.name }}</v-list-item-title>
                    </v-btn>
                  </v-list-item>
                </v-list>
              </v-expansion-panel-text>
            </v-expansion-panel>
          </v-expansion-panels>
        </div>

        <div v-if="selectedTech" class="tech-description">
          <p><strong>{{ selectedTech.name }}</strong></p>
          <p>{{ selectedTech.description }}</p>
        </div>
      </div>
    </div>
  </v-container>
</template>

<script setup lang="ts">
import { ref } from 'vue';

const files = ref([
  { name: "HTML", description: "HTML (HyperText Markup Language) é a linguagem padrão para criar páginas web." },
  { name: "CSS", description: "CSS (Cascading Style Sheets) é usado para estilizar o conteúdo das páginas web." },
  { name: "JavaScript", description: "JavaScript é uma linguagem de programação usada para criar páginas web interativas." },
  { name: "Vue.js", description: "Vue.js é um framework JavaScript para construir interfaces de usuário." },
  { name: "Quasar", description: "Quasar é um framework baseado no Vue.js para criar aplicações rápidas e responsivas." },
  { name: "Java", description: "Java é uma linguagem de programação de uso geral, amplamente utilizada em sistemas corporativos." },
  { name: "Spring Boot", description: "Spring Boot é uma ferramenta para criar aplicações Java de forma rápida e com configuração mínima." },
  { name: "Docker", description: "Docker é uma plataforma de software para criar, testar e executar aplicativos em contêineres." }
]);

interface Tech {
  name: string;
  description: string;
}

const selectedTech = ref<Tech | null>(null);
</script>

<style scoped>
.vsCopy {
  display: flex;
  background-color: #1e1e1e;
}

.vsHeader {
  display: flex;
  justify-content: center;
  align-items: center;
  width: 100%;
  height: 3rem;
  background-color: #3C3C3C;
}

.circle {
  width: 20px;
  height: 20px;
  background-color: #3C3C3C;
}

.vsSidebar {
  width: 5%;
  height: 35rem;
  background-color: #333333;
}

.vsSecondSidebar {
  background-color: #252526;
}

.no-shadow {
  box-shadow: none !important;
  border: none !important;
}

.full-btn {
  width: 100%;
  justify-content: flex-start;
  text-align: left;
}

.tech-description {
  color: white;
  padding: 10px;
  margin-left: 20px;
  border-radius: 5px;
}
</style>
