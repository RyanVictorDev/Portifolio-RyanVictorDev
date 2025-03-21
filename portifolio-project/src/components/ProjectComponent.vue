<template>
  <v-container class="componentWidth">
    <div class="image rounded-xl d-flex justify-center mb-3 pa-2" :style="{ backgroundColor: backgroundColor, backgroundImage: `linear-gradient(${backgroundColor}, rgb(3, 3, 3))` }">
      <img class="projectImage" :src="image" alt="">
    </div>

    <div class="mb-3">
      <p class="text-h6 mx-auto text-left mb-1">{{ title }}</p>
      <p class="text-body-1 font-weight-light">{{ description }}</p>
    </div>

    <v-row class="mb-1">
      <v-col v-for="tecnology in technologies" :key="tecnology" cols="auto">
        <v-card class="pa-0 bg-#212121">
          <v-card-title class="text-caption text-center text-white">
            {{ tecnology }}
          </v-card-title>
        </v-card>
      </v-col>
    </v-row>

    <a class="text-decoration-none text-grey" target="_blank" :href="projectLink">Acessar projeto -></a>
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
  projectLink: {
    type: String,
    required: false,
    default: '',
  },
});

</script>

<style scoped>
.componentWidth {
  width: 95%;
}

.image {
  width: 100%;
  max-height: fit-content;
  transition: all 1.5s;
}

.image:hover {
  background-image: radial-gradient() (rgb(0, 0, 0), rgb(37, 37, 37));
}

.projectImage {
  max-width: 100%;
  height: auto;
  /* margin-bottom: -3rem; */
  object-fit: cover;
  transition: all 0.5s;
}

.projectImage:hover {
  transform: scale(1.1);
  transform: translateY(-1.5rem);
  filter: drop-shadow(0 0 10px #ffffff7a);
}
</style>
