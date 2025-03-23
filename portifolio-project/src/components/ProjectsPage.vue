<template>
  <v-container class="">
    <p class="title mx-auto text-center mb-12 pt-12">Projetos</p>
    <v-row class="justify-space-evenly ga-12">
      <v-col cols="10" md="5">
        <ProjectComponent
          class="fade-left"
          title="Locadora de Livros - Flutter"
          description="Projeto de locadora de livros criada em Flutter e Dart. Projeto desenvolvido para estudo e primeiros passos em Flutter."
          :technologies="['Flutter', 'Dart']"
          image="/images/flutterMockupOriginal.png"
          background-color="#283593"
          project-link="https://github.com/RyanVictorDev/Locadora-Flutter"
        />

        <ProjectComponent
          class="fade-left"
          title="Locadora de Livros - Spring Boot"
          description="Backend para a Locadora de Livros criado com Java, Spring Boot e Dockerizado. Sistema com authenticação de usuários e controle de registros e estoque."
          :technologies="['Java', 'Spring Boot', 'Docker', 'Postgres']"
          image="/images/springbootMockup.png"
          background-color="#00E676"
          project-link="https://github.com/RyanVictorDev/LocadoraJava"
        />
      </v-col>

      <v-col cols="10" md="5">
        <ProjectComponent
          class="fade-left"
          title="Locadora de Livros - Quasar"
          description="Projeto Locadora de Livros desenvolvido com Vue e Quasar, testado com Robot Framework, Dockerizado e conectado com o backend Spring Boot."
          :technologies="['Vue', 'Quasar', 'Robot', 'Docker']"
          image="/images/note.png"
          background-color="#6200EA"
          project-link="https://github.com/RyanVictorDev/Locadora-Ryan"
        />

        <ProjectComponent
          class="fade-left"
          title="Matematic"
          description="Projeto concebido para auxiliar os usuários na realização e compreensão de operações matemáticas com explicações passo a passo. Desenvolvido com HTML, CSS e JavaScript."
          :technologies="['HTML', 'CSS', 'JS']"
          image="/images/matematicMockup.png"
          background-color="#4E342E"
          project-link="https://github.com/RyanVictorDev/Projeto-Matematic"
        />

        <ProjectComponent
          class="fade-left"
          title="StayOn"
          description="Projeto destinado a pessoas que estão se preparando para vestibulares como o da UECE e o ENEM. Oferece uma previsão do resultado para aqueles que já realizaram."
          :technologies="['HTML', 'CSS', 'JS']"
          image="/images/stayOnMockup.png"
          background-color="#880E4F"
          project-link="https://github.com/RyanVictorDev/Projeto-StayOn"
        />
      </v-col>
    </v-row>

    <!-- <div class="mx-auto text-center">
      <v-btn
        color="black"
        class="border"
        @click="expand"
        v-if="!expanded"
      >
        Exibir mais
      </v-btn>
    </div> -->
  </v-container>
</template>

<script setup lang="ts">
import ProjectComponent from './ProjectComponent.vue';
// import { ref } from 'vue';

// const expanded = ref(false);

// const expand = () => {
//   expanded.value = !expanded.value;
// };
</script>

<style scoped>

</style>
