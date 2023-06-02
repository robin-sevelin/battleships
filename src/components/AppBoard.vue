<script setup lang="ts">
  import { ref } from 'vue';
  import { Div } from '../models/Div';
  import AppDiv from './AppDiv.vue';
  import { Board } from '../models/Board';

  const board = ref<Board>(new Board([]));
  const div = ref<Div>();

  for (let i = 0; i < 9; i++) {
    div.value = new Div('', i);
    board.value.div.push(div.value);
  }

  const handleEmit = (payload: number) => {
    console.log('du klickade på ' + payload);
  };
</script>
<template>
  <div class="board">
    <AppDiv :div="div" v-for="div in board.div" @click="handleEmit" />
  </div>
</template>

<style scoped>
  .board {
    border: 1px solid black;
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    grid-template-rows: repeat(3, 1fr);
    grid-column-gap: 0px;
    grid-row-gap: 0px;
  }
</style>
