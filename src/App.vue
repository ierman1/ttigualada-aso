<script setup lang="ts">
import DefaultNavbar from './components/DefaultNavbar.vue';

</script>

<template>
  <header>
    <DefaultNavbar />
  </header>
  <main>
    <router-view />
  </main>
  <footer></footer>
</template>

<style scoped></style>
