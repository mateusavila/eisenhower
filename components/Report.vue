<script lang="ts" setup>
  import { useStorage } from '@vueuse/core';

  const block0 = useStorage('block0', '').value
  const block1 = useStorage('block1', '').value
  const block2 = useStorage('block2', '').value
  const block3 = useStorage('block3', '').value
</script>

<template>
  <h1>Relatório</h1>
  <hr>
  <h2>Monolito</h2>
  <h3>Tarefas Urgentes</h3>
  <div class="block-text" v-text="block0"></div>
  <h3>Tarefas não urgentes</h3>
  <div class="block-text" v-text="block1"></div>
  <h2>Serviços Distribuidos</h2>
  <h3>Tarefas Urgentes</h3>
  <div class="block-text" v-text="block2"></div>
  <h3>Tarefas não urgentes</h3>
  <div class="block-text" v-text="block3"></div>
</template>

<style lang="sass">
  .block-text
    padding: 10px 0
    font-size: 14px
    color: #404041
    white-space: pre
</style>