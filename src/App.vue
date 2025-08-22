<script setup lang="ts">
import DefaultNavbar from './components/DefaultNavbar.vue';
import DefaultFooter from './components/DefaultFooter.vue';
</script>

<template>
  <header>
    <DefaultNavbar />
  </header>
  <main>
    <router-view />
  </main>
  <footer>
    <DefaultFooter />
  </footer>
</template>

<style scoped></style>
