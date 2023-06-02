<script setup lang="ts">
  import AppBoard from './AppBoard.vue';
  defineProps<{ content: string }>();
</script>

<template>
  <main>
    <h2>{{ content }}</h2>
    <AppBoard />
  </main>
</template>

<style scoped>
  main {
    max-width: 900px;
    margin: auto;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    position: relative;
    top: 50px;
    margin-bottom: 100px;
    padding-bottom: 2rem;
  }
</style>
