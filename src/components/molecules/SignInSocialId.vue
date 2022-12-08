<script setup lang="ts">
import { onMounted, ref } from "vue"
// console.log(Intl.DateTimeFormat().resolvedOptions().timeZone)

// const result = new Intl.DisplayNames(
//   ['en'], {type: 'region'}
// );

// // ofで表示名取得
// console.log(result.of('JP')); // Japan
// console.log(result.of('US')); // United States
// console.log(result.of('AU')); // Australia
// console.log(result.of('GB')); // United Kingdom
// console.log(result.of('TW')); // Taiwan

// const request = require('request-promise')

// request('http://ip-api.io/api/json?api_key=YOUR_API_KEY')
//   .then(response => console.log(JSON.parse(response)))
//   .catch(err => console.log(err))

// import geolocation from "geolocation"
 
// geolocation.getCurrentPosition(function (err, position) {
//   if (err) throw err
//   console.log(position)
// })

  const user = ref("japan")

</script>

<template lang="pug">
form
  legend
    fieldset.-sign-in
      button.-social-login.-google
        span.mdi.mdi-google
        span Google Account
      button.-social-login.-facebook
        span.mdi.mdi-facebook
        span Facebook Account
      button.-social-login.-instagram
        span.mdi.mdi-instagram
        span Instagram Account
      button.-social-login.-twitter
        span.mdi.mdi-twitter
        span Twitter Account
      button.-social-login.-linkedin
        span.mdi.mdi-linkedin
        span LinkedIn Account
      button.-social-login.-line(
        v-if="user === 'japan'"
      )
        span.mdi.mdi-chat
        span Line Account
      button.-social-login.-kakao(
        v-else-if="user === 'korea'"
      )
        span.mdi.mdi-chat
        span Kakao Account
</template>

<style lang="sass" scoped>
.-sign-in
  position: relative
  border: none
  .-social-login
    display: inline-block
    width: 200px
    height: 48px
    float: left
    margin: 12px 6px 0
    padding: 12px
    border-radius: 24px
    background-color: var(--vt-c-blue-area-inline)
    cursor: pointer
    &:hover
      border: 3px solid var(--vt-c-blue-impact-light-hovered)
    &:nth-child(even)
      float: right
</style>