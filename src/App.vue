<script setup lang="ts">
import { RouterLink, RouterView } from 'vue-router'
import HelloWorld from './components/HelloWorld.vue'
</script>

<template lang="pug">
RouterView
</template>

<style lang="sass">
// @media (min-width: 1024px)


@import '@mdi/font/css/materialdesignicons.css' 
*,
*::before,
*::after
  box-sizing: border-box
  margin: 0
  position: relative
  font-weight: normal

button
  padding: 8px 12px
  margin: 0 0 0 12px
  color: var(--vt-c-blue-text-light)
  border: none
  border-radius: 24px
  background-color: var(--vt-c-blue-area-inline)
  &.activated
    font-weight: 700

nav
  border-bottom: 2px solid var(--vt-c-blue-area-inline)
  label
    cursor: pointer
    p
      margin: 0 0 0 12px
      margin-bottom: -2px
      padding: 8px 12px
      // border-radius: 24px
      display: inline-block
      border: 2px solid var(--vt-c-blue-area)
      border-bottom: 2px solid var(--vt-c-blue-area-inline)
      border-radius: 12px 12px 0 0
      // background: var(--vt-c-blue-area-inline)
      opacity: 0.5
    input[type="radio"]
      display: none
      &:checked ~ p
        border: 2px solid var(--vt-c-blue-area-inline)
        border-bottom: 2px solid var(--vt-c-blue-area)
        opacity: 1
input[type="checkbox"]
  display: none
  & ~ .mdi-checkbox-blank
    display: inline-block
  & ~ .mdi-checkbox-marked
    display: none
  &:checked
    & ~ .mdi-checkbox-blank
      display: none
    & ~ .mdi-checkbox-marked
      display: inline-block
label
  display: inline
.mdi
  margin-right: 4px
  // &::before
  //   content: ""
  //   display: block
  //   position: relative
  //   width: 48px
  //   height: 48px
  //   background-color: red

.noline
  border: none
</style>
