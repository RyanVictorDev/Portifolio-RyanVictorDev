<template>
  <v-container>
    <p class="title mx-auto text-center mb-12 pt-12">Projetos</p>
    <v-row class="justify-space-evenly ga-12">
      <v-col cols="8" md="5">
        <ProjectComponent
          title="Locadora de Livros - Flutter"
          description="Um projeto incrível desenvolvido com Vue e Vuetify."
          :technologies="['Flutter', 'Dart']"
          image="/images/flutterMockupOriginal.png"
          background-color="blue"
          project-link="https://github.com/RyanVictorDev/Locadora-Flutter"
        />

        <ProjectComponent
          title="Locadora de Livros - Flutter"
          description="Um projeto incrível desenvolvido com Vue e Vuetify."
          :technologies="['Flutter', 'Dart']"
          image="/images/note.png"
          background-color="red"
          project-link="https://github.com/RyanVictorDev/Locadora-Ryan"
        />
      </v-col>
      <v-col cols="8" md="5">
        <ProjectComponent
          title="Locadora de Livros - Quasar"
          description="Um projeto incrível desenvolvido com Vue e Vuetify."
          :technologies="['Vue', 'Quasar', 'Robot', 'Docker']"
          image="/images/note.png"
          background-color="purple"
          project-link="https://github.com/RyanVictorDev/Locadora-Ryan"
        />

        <ProjectComponent
          title="Locadora de Livros - Flutter"
          description="Um projeto incrível desenvolvido com Vue e Vuetify."
          :technologies="['Flutter', 'Dart']"
          image="/images/flutterMockupOriginal.png"
          background-color="green"
        />
      </v-col>
    </v-row>
  </v-container>
</template>

<script setup lang="ts">
import ProjectComponent from './ProjectComponent.vue';

</script>
