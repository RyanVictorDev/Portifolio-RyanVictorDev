<template>
  <v-container>
    <div class="image rounded-xl d-flex justify-center mb-3 pa-2" :style="{ backgroundColor: backgroundColor }">
      <img class="projectImage" :src="image" alt="">
    </div>

    <div class="mb-3">
      <p class="text-h6 mx-auto text-left mb-1">{{ title }}</p>
      <p class="text-body-1 font-weight-light">{{ description }}</p>
    </div>

    <v-row>
      <v-col v-for="tecnology in technologies" :key="tecnology" cols="auto">
        <v-card class="pa-0 bg-#212121">
          <v-card-title class="text-body-2 text-center text-white">
            {{ tecnology }}
          </v-card-title>
        </v-card>
      </v-col>
    </v-row>
  </v-container>
</template>

<script setup lang="ts">
defineProps({
  title: {
    type: String,
    required: true,
  },
  description: {
    type: String,
    required: true,
  },
  technologies: {
    type: Array as () => string[],
    required: true,
  },
  image: {
    type: String,
    required: true,
  },
  backgroundColor: {
    type: String,
    required: false,
    default: '#fff',
  },
});

</script>

<style scoped>
.image {
  width: 100%;
  min-height: fit-content;
}

.projectImage {
  max-width: 100%;
  height: auto;
  object-fit: contain;
}
</style>
