<script setup lang="ts">
import AppBar from './components/AppBar.vue'
import MainCard from './components/MainCard.vue'
</script>

<template>
  <v-layout>
    <AppBar />
    <v-main>
      <v-container fluid>
        <v-row justify="center" class="ma-4">
          <MainCard />
        </v-row>
      </v-container>
    </v-main>
  </v-layout>
</template>
