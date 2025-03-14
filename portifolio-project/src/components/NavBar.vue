<template>
  <div class="nav-bar mx-auto mt- rounded-xl border">
    <v-btn class="nav-link text-body-2" text="Home" variant="text"/>
    <v-btn class="nav-link text-body-2" text="Experiências" variant="text"/>
    <v-btn class="nav-link text-body-2" text="Competências" variant="text"/>
    <v-btn class="nav-link text-body-2" text="Projetos" variant="text"/>
    <v-btn class="nav-link text-body-2" text="Contato" variant="text"/>
  </div>
</template>

<script lang="ts" setup>

</script>

<style scoped>
.nav-bar {
  display: flex;
  max-width: 40%;
  justify-content: space-around;
  padding: 0.1rem;
  background-color: #2b2b2b6e;
  position: fixed;
  z-index: 100;
  left: 50%;
  top: 1rem;
  transform: translateX(-50%);
}
</style>
