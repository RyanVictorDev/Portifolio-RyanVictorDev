<template>
  <v-carousel
    hide-delimiters
    height="400"
    show-arrows="hover"
    cycle
    hide-delimiter-background
    class="rounded-lg"
  >
    <v-carousel-item
      v-for="(slide, i) in slides"
      :key="i"
    >
      <v-sheet
        :color="slide.color"
        height="100%"
      >
        <div class="d-flex fill-height justify-center align-center">
          <div class="text-h2 text-center">
            <v-icon>{{ slide.icon }}</v-icon>
            <p class="mt-3 text-body-1">{{ slide.title }}</p>
          </div>
        </div>
      </v-sheet>
    </v-carousel-item>
  </v-carousel>
</template>

<script lang="ts" setup>
  const slides = [
    {
      title: 'HTML5',
      icon: 'mdi-language-html5',
      color: 'deep-orange-darken-3',
    },
    {
      title: 'CSS3',
      icon: 'mdi-language-css3',
      color: 'cyan-darken-4',
    },
    {
      title: 'JavaScript',
      icon: 'mdi-language-javascript',
      color: 'yellow-darken-2',
    },
    {
      title: 'Vue.js',
      icon: 'mdi-vuejs',
      color: 'green-accent-4',
    },
    {
      title: 'Quasar',
      icon: 'mdi-lightning-bolt-outline',
      color: 'indigo-accent-3',
    },
    {
      title: 'Java',
      icon: 'mdi-language-java',
      color: 'deep-purple accent-4',
    },
    {
      title: 'Spring Boot',
      icon: 'mdi-sprout',
      color: 'green-darken-4',
    },
    {
      title: 'Docker',
      icon: 'mdi-docker',
      color: 'blue-darken-4',
    },
    {
      title: 'GitHub',
      icon: 'mdi-github',
      color: 'black',
    },
    {
      title: 'Git',
      icon: 'mdi-git',
      color: 'orange-darken-4',
    },
    {
      title: 'PostgreSQL',
      icon: 'mdi-database',
      color: 'blue-accent-4',
    },
    {
      title: 'Figma',
      icon: 'mdi-palette',
      color: 'purple-darken-4',
    }
  ]
</script>
