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
        <p class="align-center mx-auto position-absolute">Front-end</p>
      </div>

      <div class="d-flex flex-row">
        <div class="d-flex flex-column rounded-bs-lg ga-2 vsSidebar">
          <v-btn class="mx-auto" icon="$vuetify" variant="text" />
          <v-btn class="mx-auto" icon="$vuetify" variant="text" />
          <v-btn class="mx-auto" icon="$vuetify" variant="text" />
        </div>

        <div class="d-flex flex-column vsSecondSidebar">
          <p class="align-left pl-6 mt-2">Explorer</p>

          <v-expansion-panels class="bg-trasparent pa-0 teste" variant="accordion">
            <v-expansion-panel class="bg-transparent teste" title="Competências">
              <v-expansion-panel-text>
                <v-list class="bg-transparent">
                  <v-list-item v-for="file in files" :key="file">
                    <v-btn class="bg-transparent border-0">
                      <v-list-item-title>{{ file }}</v-list-item-title>
                    </v-btn>
                  </v-list-item>
                </v-list>
              </v-expansion-panel-text>
            </v-expansion-panel>
          </v-expansion-panels>
        </div>
      </div>
    </div>
  </v-container>
</template>

<script setup lang="ts">
import { ref } from 'vue';

const files = ref([
  "html",
  "css",
  "js",
  "vue",
  "quasar",
  "java",
  "spring",
  "docker",
]);
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

.teste{
  min-width: 100%;
}
</style>
