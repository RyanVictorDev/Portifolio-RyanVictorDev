<template>
  <v-container fluid class="fill-height pa-0">
    <v-responsive class="d-flex align-center video-background" height="100vh">
      <video autoplay loop muted playsinline class="background-video">
        <source src="../assets/black-and-white-waves.1920x1080.mp4" type="video/mp4" />
      </video>

      <div class="d-flex my-auto content-overlay">
        <v-row class="mx-auto justify-center">
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
      </div>
    </v-responsive>
  </v-container>
</template>

<script setup lang="ts">
  import Typewriter from './TypewriterEffect.vue';
</script>

<style>
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
  /* text-align: center; */
}
</style>
