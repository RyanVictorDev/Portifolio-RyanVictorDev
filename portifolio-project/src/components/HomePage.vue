<template>
  <v-container fluid class="fill-height pa-0">
    <v-responsive class="d-flex align-center video-background" height="100vh">
      <video autoplay loop muted playsinline class="background-video">
        <source src="../assets/black-and-white-waves.1920x1080.mp4" type="video/mp4" />
      </video>

      <div class="d-flex my-auto content-overlay">
        <v-row v-if="display.mdAndUp.value" class="mx-auto justify-center">
          <v-col class="text-center my-auto mx-auto" cols="7">
            <div class="mb-4">
              <h1 class="text-h2 text-left font-weight-medium">RYAN VICTOR</h1>
              <Typewriter />
            </div>
            <div class="text-body-1 font-weight-light text-left text-grey-lighten-1">Olá, sou Ryan Victor, desenvolvedor full stack apaixonado por tecnologia. Trabalho com Vue.js, Quasar, Java e Spring Boot, criando soluções web rápidas e eficientes. Sempre em busca de novos desafios, estou pronto para transformar ideias em realidade.</div>
          </v-col>

          <v-col class="my-auto mx-auto" cols="3">
            <v-img
              class="my-auto"
              height="300"
              src="@/assets/ryan.png"
            />
          </v-col>
        </v-row>

        <v-row v-else lass="mx-auto justify-center">
          <v-col class="my-auto mx-auto" cols="8">
            <v-img
              class="my-auto"
              height="200"
              src="@/assets/ryan.png"
            />
          </v-col>

          <v-col class="text-center my-auto mx-auto" cols="8">
            <div class="mb-4">
              <h1 class="text-h5 text-left font-weight-medium">RYAN VICTOR</h1>
              <Typewriter
                font="text-body-2"
              />
            </div>
            <div class="text-body-2 font-weight-light text-left text-grey-lighten-1">Olá, sou Ryan Victor, desenvolvedor full stack apaixonado por tecnologia. Trabalho com Vue.js, Quasar, Java e Spring Boot, criando soluções web rápidas e eficientes. Sempre em busca de novos desafios, estou pronto para transformar ideias em realidade.</div>
          </v-col>
        </v-row>
      </div>

      <div class="d-flex ga-12 justify-center button-container">
        <div>
          <v-btn class="button mx-auto rounded-pill border" color="transparent" dark target="_blank" href="https://github.com/RyanVictorDev">
            <v-icon size="large">mdi-github</v-icon>
          </v-btn>
        </div>

        <div>
          <v-btn class="button mx-auto rounded-pill border" color="transparent" dark target="_blank" href="https://www.linkedin.com/in/ryan-victor-dev">
            <v-icon size="large">mdi-linkedin</v-icon>
          </v-btn>
        </div>

        <div>
          <v-btn class="button mx-auto rounded-pill border" color="transparent" dark href="">
            <v-icon size="large">mdi-file-account</v-icon>
          </v-btn>
        </div>
      </div>
    </v-responsive>
  </v-container>
</template>

<script setup lang="ts">
  import Typewriter from './TypewriterEffect.vue';
  import { useDisplay } from 'vuetify';

  const display = useDisplay();
</script>

<style scoped>
.video-background {
  position: relative;
  width: 100%;
  height: 100vh;
  overflow: hidden;
}

.background-video {
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  min-width: 100%;
  min-height: 100%;
  object-fit: cover;
  z-index: 0;
  opacity: 0.2;
}

.content-overlay {
  position: relative;
  z-index: 2;
  width: 100%;
}

.button-container {
  position: absolute;
  bottom: 30px;
  left: 50%;
  transform: translateX(-50%);
  display: flex;
  gap: 12px;
  z-index: 3;
}

.button{
  width: 50px;
  height: 60px;
}
</style>
