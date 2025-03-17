<template>
  <v-container>
    <p class="title mx-auto text-center mb-12 pt-12">Projetos</p>
    <v-row class="justify-space-between">
      <v-col class="" cols="5">
        <ProjectComponent
          title="Locadora de Livros - Flutter"
          description="Um projeto incrível desenvolvido com Vue e Vuetify."
          :technologies="['Flutter', 'Dart']"
          image="/images/flutterMockupOriginal.png"
          background-color="blue"
        />
      </v-col>
      <v-col cols="5">
        <ProjectComponent
          title="Locadora de Livros - Flutter"
          description="Um projeto incrível desenvolvido com Vue e Vuetify."
          :technologies="['Flutter', 'Dart']"
          image="/images/flutterMockupOriginal.png"
          background-color="blue"
        />
      </v-col>
    </v-row>
  </v-container>
</template>

<script setup lang="ts">
import ProjectComponent from './ProjectComponent.vue';

</script>
