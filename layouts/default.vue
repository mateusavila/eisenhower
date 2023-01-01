<template>
  <div class="default-page">
    <slot />
  </div>
</template>

<style lang="sass">
  html, body
    margin: 0
    padding: 0
  html
    background: #fafafa
    font-family: Lato
  *, *:before, *:after
    box-sizing: border-box
  .container
    width: calc(100% - 40px)
    max-width: 1200px
    margin: 0 auto
</style>