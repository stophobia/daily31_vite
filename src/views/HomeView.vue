<script setup lang="ts">
import Home from '../components/organisms/Home.vue'
</script>

<template lang="pug">
main.main
  Home.-content.-home
</template>

<style lang="sass">
.main
  display: flex
  justify-content: center
  align-items: center
  width: 100vw
  height: 100vh
  background-color: var(--vt-c-blue-background)
  .-content
    background-color: var(--vt-c-blue-area)
    border-radius: 12px
    &.-home
      width: 500px
</style>
