<template>
  <div class="nav-bar mx-auto mt- rounded-xl border px-6">
    <!-- <v-btn class="nav-link text-body-2" text="Home" variant="text"/>
    <v-btn class="nav-link text-body-2" text="Experiências" variant="text"/>
    <v-btn class="nav-link text-body-2" text="Competências" variant="text"/>
    <v-btn class="nav-link text-body-2" text="Projetos" variant="text"/>
    <v-btn class="nav-link text-body-2" text="Contato" variant="text"/> -->

    <v-tabs
      v-model="tabs"
      slider-color="purple"
    >
      <v-tab class="v-tab text-body-2 pa-0" text="Home" value="one"></v-tab>

      <v-tab class="v-tab text-body-2" text="Experiências" value="two"></v-tab>

      <v-tab class="v-tab text-body-2" text="Competências" value="three"></v-tab>

      <v-tab class="v-tab text-body-2" text="Projetos" value="four"></v-tab>

      <v-tab class="v-tab text-body-2" text="Contato" value="five"></v-tab>
    </v-tabs>
  </div>
</template>

<script lang="ts" setup>
  import { computed, ref } from 'vue'

  const tabs = ref(null)
</script>

<style scoped>
.nav-bar {
  display: flex;
  max-width: 45%;
  /* justify-content: space-around; */
  padding: 0.1rem;
  background-color: #2b2b2b6e;
  position: fixed;
  z-index: 100;
  left: 50%;
  top: 1rem;
  transform: translateX(-50%);
}

.v-tab {
  padding: 4px 8px !important; /* Menos espaçamento interno */
  min-width: auto !important; /* Removendo largura mínima padrão */
}
</style>
