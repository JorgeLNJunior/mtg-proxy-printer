<script lang="ts" setup>
import { ref } from 'vue'

import { deckExample } from '../texts/texts'

const deck = ref<string>('')

function clear(): void {
  deck.value = ''
}
</script>

<template>
  <v-card class="text-center pa-2" elevation="2" rounded>
    <v-card-title class="select-none">Deck</v-card-title>
    <v-card-subtitle class="select-none">
      Insira o deck no formato
      <a
        class="text-decoration-none"
        href="https://www.mtggoldfish.com/deck/arena_download/5211385"
        target="_blank"
        rel="noopener noreferrer"
      >
        <b>padrão</b>
      </a>
      do Magic Arena. As cartas
      <b>devem</b>
      estar em Inglês.
    </v-card-subtitle>
    <v-card-text>
      <v-textarea
        v-model="deck"
        :no-resize="true"
        :auto-grow="true"
        :placeholder="deckExample"
      ></v-textarea>
    </v-card-text>
    <v-card-actions>
      <v-btn color="primary" variant="flat">Enviar</v-btn>
      <v-btn color="accent" @click="clear()">Limpar</v-btn>
    </v-card-actions>
  </v-card>
</template>
