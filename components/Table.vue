<script lang="ts" setup>
  import { useStorage } from '@vueuse/core';

  const block0 = useStorage('block0', '')
  const block1 = useStorage('block1', '')
  const block2 = useStorage('block2', '')
  const block3 = useStorage('block3', '')
</script>

<template>
  <table class="table">
    <thead>
      <tr>
        <th></th>
        <th class="th">Urgente (1o Trimestre)</th>
        <th class="th">Não Urgente (2o Trimestre)</th>
      </tr>
    </thead>
    <tbody>
      <tr>
        <th class="tbody-th"><span>Monolito</span></th>
        <td class="tbody-td">
          <textarea 
            :class="`textarea-0`" 
            v-model="block0" />
        </td>
        <td class="tbody-td">
          <textarea 
            :class="`textarea-1`" 
            v-model="block1" />
        </td>
      </tr>
      <tr>
        <th class="tbody-th"><span>Serviços Distribuidos</span></th>
        <td class="tbody-td">
          <textarea 
            :class="`textarea-2`" 
            v-model="block2" />
        </td>
        <td class="tbody-td">
          <textarea 
            :class="`textarea-3`" 
            v-model="block3" />
        </td>
      </tr>
    </tbody>
  </table>
</template>

<style lang="sass">
  .table
    width: 100%
    margin: 30px 0
    thead
      th
        padding: 10px
      .th
        background: #dadada
    tbody
      .tbody-th
        vertical-align: middle
        background: #dadada
    .tbody-td
      min-width: calc(50% - 30px)
      max-width: calc(50% - 30px)
      width: 50%
      height: 300px
      border: 1px solid #ccc
      padding: 5px
      font-size: 14px
      font-family: Lato
      color: #333
      vertical-align: top
      position: relative
      textarea
        width: 100%
        height: 100%
        font-family: Lato
        font-size: 14px
        color: #333
        padding: 5px
        position: absolute
        top: 0
        left: 0
        resize: none
        border-width: 1px
        border-style: solid
        &.textarea-0
          background: #00D08A
          border-color: #00D08A
        &.textarea-1
          background: #F0D663
          border-color: #F0D663
        &.textarea-2
          background: #008AA2
          border-color: #008AA2
          color: #fff
        &.textarea-3
          background: #D02C00
          border-color: #D02C00
          color: #fff
</style>