<template>
  <v-container>
    <div
      class="image rounded-lg mb-3"
      :style="{ backgroundImage: `url(${image})` }"
    ></div>

    <div class="mb-3">
      <p class="text-h6 mx-auto text-left mb-1">{{ title }}</p>
      <p class="text-body-1 font-weight-light">{{ description }}</p>
    </div>

    <v-row>
      <v-col v-for="tecnology in technologies" :key="tecnology" cols="auto">
        <v-card class="px-2 bg-#212121">
          <v-card-title class="text-center text-white">
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
});
</script>

<style scoped>
.image {
  width: 100%;
  height: 450px;
  background-size: cover;
  background-position: center;
}
</style>
