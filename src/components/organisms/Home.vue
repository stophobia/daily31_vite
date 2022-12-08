<script setup lang="ts">
import SignInEmail from '../molecules/SignInEmail.vue'
import SignInSocialId from '../molecules/SignInSocialId.vue'
import { onMounted, ref } from "vue"

let sign_in_method = ref("email")

const selectMethod = (selected_method: string) => {
  sign_in_method.value = selected_method
}
</script>

<template lang="pug">
div.login
  nav Sign in with
    label(
      @click="selectMethod('email')"
    )
      input#email.radio(
        v-if="sign_in_method === 'email'"
        name="sign_in"
        type="radio"
        checked
      )
      input#email.radio(
        v-else
        name="sign_in"
        type="radio"
      )
      p 
        span.mdi.mdi-email
        | Email
    label(
      @click="selectMethod('social_id')"
    )
      input#socialid.radio(
        v-if="sign_in_method === 'social_id'"
        name="sign_in"
        type="radio"
        checked
      )
      input#socialid.radio(
        v-else
        name="sign_in"
        type="radio"
      )
      p 
        span.mdi.mdi-google-circles-communities
        | Social ID
  SignInEmail(
    v-if="sign_in_method === 'email'"
  )
  SignInSocialId(
    v-else-if="sign_in_method === 'social_id'"
  )
</template>

<style lang="sass" scoped>
.login
  padding: 12px 0
  width: 500px
  height: 284px
  border-radius: 8px
  padding: 24px
</style>
