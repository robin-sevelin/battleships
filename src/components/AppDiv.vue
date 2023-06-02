<script setup lang="ts">
  import { IDivProps } from '../models/IDivProps';

  const divProps = defineProps<IDivProps>();

  const emits = defineEmits(['click']);

  const handleCLick = (divId: number) => {
    emits('click', divId);
  };
</script>

<template>
  <div class="div" @click="handleCLick(divProps.div.id)">
    {{ divProps.div.id }}
  </div>
</template>

<style scoped>
  .div {
    border: 1px solid black;
    width: 110px;
    height: 110px;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    font-size: 2rem;
    background-color: white;
  }
</style>
