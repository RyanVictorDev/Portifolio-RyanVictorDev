<template>
  <v-app-bar :elevation="1" rounded color="black">
    <v-app-bar-title>Ryan Victor</v-app-bar-title>

    <template v-slot:append>
      <v-btn class="nav-link text-body-2" text="Home" variant="text"></v-btn>
      <v-btn class="nav-link text-body-2" text="Experiências" variant="text"></v-btn>
      <v-btn class="nav-link text-body-2" text="Competências" variant="text"></v-btn>
      <v-btn class="nav-link text-body-2" text="Projetos" variant="text"></v-btn>
      <v-btn class="nav-link text-body-2" text="Contato" variant="text"></v-btn>
    </template>
  </v-app-bar>
</template>
