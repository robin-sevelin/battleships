<script setup lang="ts">
  defineProps<{ content: string }>();
</script>

<template>
  <footer>
    <h2>{{ content }}</h2>
  </footer>
</template>

<style scoped>
  footer {
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    width: 100%;
    position: absolute;
    bottom: 0;
  }

  .img-container {
    display: flex;
    gap: 1rem;
    padding: 1rem;
    padding: 1rem;
  }
</style>
