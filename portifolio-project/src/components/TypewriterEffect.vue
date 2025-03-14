<script lang="ts" setup>
import { ref, onMounted } from 'vue';
// @ts-expect-error: Typewriter does not have TypeScript definitions
import Typewriter from 'typewriter-effect/dist/core';

const typewriterElement = ref(null);

const texts = [
  "DESENVOLVEDOR FULL STACK",
  "FREE LANCER",
  "TÉCNICO EM INFORMÁTICA",
];

onMounted(() => {
  new Typewriter(typewriterElement.value, {
    loop: true,
    delay: 50,
    deleteSpeed: 25,
  })
    .callFunction(() => console.log("Iniciando Typewriter"))
    .pauseFor(1000)
    .typeString(texts[0])
    .pauseFor(1500)
    .deleteAll()
    .typeString(texts[1])
    .pauseFor(1500)
    .deleteAll()
    .typeString(texts[2])
    .pauseFor(1500)
    .deleteAll()
    .start();
});
</script>

<template>
  <v-container class="d-flex justify-left align-left text-left pa-0">
    <v-card class="bg-transparent d-flex">
      <p class="text-h6 font-weight-medium pr-1">SOU</p>
      <p class="text-h6 font-weight-medium" ref="typewriterElement"></p>
    </v-card>
  </v-container>
</template>
