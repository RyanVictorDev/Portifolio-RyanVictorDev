<script lang="ts" setup>
import { ref, onMounted } from 'vue';
// @ts-expect-error: Typewriter does not have TypeScript definitions
import Typewriter from 'typewriter-effect/dist/core';

const typewriterElement = ref(null);

const props = defineProps({
  texts: {
    type: Array as () => string[],
    required: false,
    default: () => [  "DESENVOLVEDOR FULL STACK", "FREE LANCER", "TÉCNICO EM INFORMÁTICA",],
  },
  font: {
    type: String,
    required: false,
    default: "text-h6",
  },
});

onMounted(() => {
  new Typewriter(typewriterElement.value, {
    loop: true,
    delay: 50,
    deleteSpeed: 25,
  })
    .callFunction(() => console.log("Iniciando Typewriter"))
    .pauseFor(1000)
    .typeString(props.texts[0])
    .pauseFor(1500)
    .deleteAll()
    .typeString(props.texts[1])
    .pauseFor(1500)
    .deleteAll()
    .typeString(props.texts[2])
    .pauseFor(1500)
    .deleteAll()
    .start();
});
</script>

<template>
  <v-container class="d-flex justify-left align-left text-left pa-0">
    <v-card class="bg-transparent d-flex">
      <p :class="`${props.font} font-weight-medium pr-1`">SOU</p>
      <p :class="`${props.font} font-weight-medium`" ref="typewriterElement"></p>
    </v-card>
  </v-container>
</template>
