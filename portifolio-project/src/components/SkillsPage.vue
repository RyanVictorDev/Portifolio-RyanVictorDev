<template>
  <v-container>
    <p class="title mx-auto text-center mb-12">Competências</p>

    <div class="vsCopy d-flex flex-column rounded-lg">
      <div class="vsHeader rounded-t-lg">
        <div class="d-flex ml-3 mr-auto ga-1">
          <div class="circle bg-red rounded-circle" />
          <div class="circle bg-yellow rounded-circle" />
          <div class="circle bg-green rounded-circle" />
        </div>
        <p class="align-center mx-auto position-absolute">Front-end</p>
      </div>

      <div class="d-flex flex-row">
        <div class="d-flex flex-column rounded-bs-lg ga-2 vsSidebar">
          <v-btn class="mx-auto" icon="$vuetify" variant="text" />
          <v-btn class="mx-auto" icon="$vuetify" variant="text" />
          <v-btn class="mx-auto" icon="$vuetify" variant="text" />
        </div>

        <div class="d-flex flex-column px-6 vsSecondSidebar">
          <p class="align-left">Explorer</p>
        </div>
      </div>
    </div>
  </v-container>
</template>

<script setup lang="ts">

</script>

<style scoped>
  .vsCopy {
    display: flex;
    background-color: #1e1e1e;
    /* height: 250px; */
  }

  .vsHeader{
    display: flex;
    justify-content: center;
    align-items: center;
    width: 100%;
    height: 3rem;
    background-color: #3C3C3C;
  }

  .circle{
    width: 20px;
    height: 20px;
    background-color: #3C3C3C;
  }

  .vsSidebar{
    width: 5%;
    height: 100%;
    background-color: #333333;
  }

  .vsSecondSidebar{
    background-color: #252526;
  }
</style>
