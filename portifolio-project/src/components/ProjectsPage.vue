<template>
  <v-container>
    <p class="title mx-auto text-center mb-12">Projetos</p>
    <v-row class="justify-space-between">
      <v-col class="" cols="5">
        <ProjectComponent
          title="Meu Projeto"
          description="Um projeto incrível desenvolvido com Vue e Vuetify."
          :technologies="['HTML', 'CSS', 'JavaScript']"
          image="../assets/ryan.png"
        />
      </v-col>
      <v-col class="bg-blue" cols="5">
        teste
      </v-col>
    </v-row>
  </v-container>
</template>

<script setup lang="ts">
import ProjectComponent from './ProjectComponent.vue';

</script>
