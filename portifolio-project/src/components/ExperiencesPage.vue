<template>
  <v-container>
    <p class="title mx-auto text-center mb-12 pt-12">Experiências</p>

    <v-row v-if="display.mdAndUp.value">
      <v-col class="d-flex flex-column justify-start border-e-md" cols="3">
        <v-btn
          v-for="(item, index) in menuItems"
          :key="index"
          class="menu-item"
          :class="{ 'active': selectedButton === item }"
          variant="text"
          align="start"
          @click="selectedButton = item"
        >
          {{ item }}
        </v-btn>
      </v-col>

      <v-col class="d-flex flex-column">
        <v-card class="overflow-auto bg-black" height="200">
          <div class="d-flex justify-between align-center">
            <v-card-title>{{ cards[selectedButton]?.title }}</v-card-title>
            <v-card-subtitle class="ml-auto">{{ cards[selectedButton]?.subtitle }}</v-card-subtitle>
          </div>
          <v-card-title class="text-purple-lighten-1">{{ cards[selectedButton]?.company }}</v-card-title>
          <v-card-text class="text-grey-lighten-1">
            <p>{{ cards[selectedButton]?.description }}</p>
          </v-card-text>
        </v-card>
      </v-col>
    </v-row>

    <v-row v-else>
      <v-col class="d-flex mx-auto flex-column border-b-md" cols="9">
        <v-btn
          v-for="(item, index) in menuItems"
          :key="index"
          class="menu-item"
          :class="{ 'active': selectedButton === item }"
          variant="text"
          align="start"
          @click="selectedButton = item"
        >
          {{ item }}
        </v-btn>
      </v-col>

      <v-col class="d-flex flex-column" cols="12">
        <v-card class="overflow-auto bg-black" height="200">
          <div class="d-flex flex-column justify-between align-center">
            <v-card-title class="mr-auto text-body-2">{{ cards[selectedButton]?.title }}</v-card-title>
            <v-card-subtitle class="mr-auto text-caption">{{ cards[selectedButton]?.subtitle }}</v-card-subtitle>
          </div>

          <v-card-title class="text-purple-lighten-1 text-body-1">{{ cards[selectedButton]?.company }}</v-card-title>
          <v-card-text class="text-grey-lighten-1 text-body-2">
            <p>{{ cards[selectedButton]?.description }}</p>
          </v-card-text>
        </v-card>
      </v-col>
    </v-row>
  </v-container>
</template>

<script setup lang="ts">
import { ref } from 'vue';
import { useDisplay } from 'vuetify';

const display = useDisplay();

const cards = {
  "WDA Tecnologia e Inovação": {
    title: "Desenvolvedor Full Stack",
    subtitle: "Ago 2024 - Presente",
    company: "WDA Group",
    description: "Como estagiário, tive a oportunidade de aprimorar diversos conhecimentos técnicos e expandir minhas habilidades no desenvolvimento de software. Meu trabalho começou com o levantamento de requisitos, onde aprendi a entender as necessidades do cliente e traduzi-las em soluções técnicas. Em seguida, aprofundei meus conhecimentos em Design, buscando sempre criar interfaces agradáveis e funcionais, focadas na melhor experiência para o usuário. Com isso, passei a trabalhar na prototipação de interfaces utilizando o Figma, o que me permitiu transformar as ideias e requisitos em modelos visuais de forma rápida e eficiente. No desenvolvimento, tive a chance de trabalhar com o Quasar Framework, criando interfaces dinâmicas e responsivas, além de trabalhar com o Spring Boot para desenvolvimento back-end, onde aprimorei meus conhecimentos em Java. Também tive a oportunidade de aplicar o Flutter no desenvolvimento de aplicativos móveis, ampliando minha visão sobre o desenvolvimento cross-platform. Por fim, fui envolvido em processos de testes, tanto unitários quanto de interface, o que me permitiu entender a importância de garantir a qualidade do código e das interfaces antes de seu lançamento."
  },
  "Experiências": {
    title: "AAAAAAAAAAAAAAAAAAAAAAAAAAAAAA",
    subtitle: "Ago 1890 - 2023",
    company: "Alguma outra empresa",
    description: "Desenvolvimento de aplicações web com Vue.js, Quasar, Java e Spring Boot."
  },
} as const;

const menuItems = Object.keys(cards) as (keyof typeof cards)[];

const selectedButton = ref<keyof typeof cards>(menuItems[0]);
</script>

<style scoped>

.menu-item {
  justify-content: flex-start;
  text-align: left;
  transition: all 0.5s;
}

.menu-item.active {
  color: #AB47BC !important;
  font-weight: bold;
}

.v-card::-webkit-scrollbar {
  width: 6px;
}

.v-card::-webkit-scrollbar-track {
  background: #222;
  border-radius: 10px;
}

.v-card::-webkit-scrollbar-thumb {
  background: #AB47BC;
  border-radius: 10px;
}

.v-card::-webkit-scrollbar-thumb:hover {
  background: #8E24AA;
}

</style>
