<script lang="ts" setup>
  const route = useRoute()
  const path = route.path
</script>

<template>
  <header>
    <div class="container">
      <div class="header-box">
        <h1>Eisenhower Box</h1>
        <p>Ajustando prioridades para o AfiliaPay 2023</p>
      </div>
      <NuxtLink v-if="path !== '/relatorio'" to="/relatorio" class="button">Gerar
        Relatório</NuxtLink>
      <NuxtLink v-else to="/" class="button">Voltar</NuxtLink>
    </div>
  </header>
</template>

<style lang="sass">
  .button
    background-color: #00c4a7
    cursor: pointer
    border-radius: 4px
    color: #fff
    padding: 8px 16px
    border: none
    font-size: 16px
    text-decoration: none
    white-space: nowrap
    transition: all .2s ease-in-out
    &:hover
      background: darken(#00c4a7, 10%)
      transition: all .2s ease-in-out
  header
    height: 80px
    background: #ededed
    width: 100%
    .container
      height: 100%
      display: flex
      align-items: center
    .header-box
      width: 100%
    p
      font-size: 14px
      margin: 0
    h1
      font-size: 25px
      color: #313131
      margin: 0 0 1px
</style>