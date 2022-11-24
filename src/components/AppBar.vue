<script lang="ts" setup>
import { useTheme } from 'vuetify'

const theme = useTheme()

function toggleTheme() {
  theme.global.name.value = theme.global.current.value.dark ? 'light' : 'dark'
}
</script>

<template>
  <v-app-bar color="primary">
    <v-app-bar-title class="select-none">Proxy Printer</v-app-bar-title>
    <v-btn
      icon
      href="https://github.com/JorgeLNJunior/mtg-proxy-printer"
      target="_blank"
      rel="noopener noreferrer"
    >
      <v-icon>mdi-github</v-icon>
    </v-btn>
    <v-btn icon @click="toggleTheme()">
      <v-icon>mdi-theme-light-dark</v-icon>
    </v-btn>
  </v-app-bar>
</template>
