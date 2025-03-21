<template>
  <v-container class="d-flex flex-column fill-height">
    <p class="title mx-auto text-center mb-12 pt-12">Contato</p>

    <v-card class="pa-6 rounded-lg card reveal">
      <v-card-title class="text-h5 text-center mb-6">Entre em Contato</v-card-title>

      <v-form ref="form" v-model="valid" lazy-validation>
        <v-text-field
          v-model="name"
          label="Nome"
          required
          :rules="[rules.required]"
        />

        <v-textarea
          v-model="message"
          label="Mensagem"
          required
          :rules="[rules.required]"
        />

        <div class="d-flex ga-3 mx-auto sendButton">
          <v-btn
            class="text-body-2"
            color="grey-darken-3"
            block
            @click="cancelEmail"
          >
            Cancelar
          </v-btn>

          <v-btn
            class="text-body-2"
            :disabled="!valid"
            color="purple"
            block
            @click="sendEmail"
          >
            Enviar
          </v-btn>
        </div>
      </v-form>
    </v-card>
  </v-container>
</template>

<script setup lang="ts">
import { ref } from 'vue';
import { onMounted } from 'vue';
import ScrollReveal from 'scrollreveal';

onMounted(() => {
  ScrollReveal().reveal(".reveal", {
    duration: 1000,
    origin: "bottom",
    distance: "50px",
    delay: 200,
    reset: false,
  });

  ScrollReveal().reveal(".fade-left", {
    duration: 1200,
    origin: "left",
    distance: "100px",
    delay: 300,
  });

  ScrollReveal().reveal(".fade-right", {
    duration: 1200,
    origin: "right",
    distance: "100px",
    delay: 300,
  });
});

const name = ref('');
const message = ref('');
const valid = ref(false);

const rules = {
  required: (value: string) => !!value || 'Campo obrigatório',
  email: (value: string) => /.+@.+\..+/.test(value) || 'E-mail inválido',
};

const sendEmail = () => {
  const subject = encodeURIComponent(`Contato de ${name.value}`);
  const body = encodeURIComponent(`Assunto: ${message.value}`);
  window.location.href = `mailto:vryan8294@gmail.com?subject=${subject}&body=${body}`;
};

const cancelEmail = () => {
  name.value = '';
  message.value = '';
};
</script>

<style scoped>
.card {
  min-width: 60%;
  max-width: 90%;
  background-color: rgba(53, 53, 53, 0.274);
}

.sendButton {
  width: 30%;
}
</style>
