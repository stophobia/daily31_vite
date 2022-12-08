<template lang="pug">
form
  legend
    fieldset.-sign-in
      dl.-id
        dt
          p.-title ID
        dd
          input.text.-input(
            type="text"
            placeholder="Input ID"
          )
      dl.-pw
        dt
          p.-title PW
        dd
          input.password.-input(
            type="password"
            placeholder="Input Password"
          )
      button.-sign-in Sign in
      label.-remember-me
        input#remember.checkbox(
          name="remember_password"
          type="checkbox"
        )
        span.mdi.mdi-checkbox-blank
        span.mdi.mdi-checkbox-marked
        span Remember Me
      a.-forget-pw
        span.mdi.mdi-key
        | Forget your password?
      a.-sign-up
        span.mdi.mdi-account
        | Sign up
</template>

<style lang="sass" scoped>
.-sign-in
  position: relative
  border: none
  padding: 12px
  .-id,
  .-pw
    position: relative
    width: 280px
    height: 48px
    padding: 12px 24px
    margin-bottom: 24px
    border-radius: 48px
    background-color: var(--vt-c-blue-area-inline)
    .-title
      position: absolute
      top: 0
      left: 0
      width: 40px
    .-input
      width: 180px
      top: 0
      left: 40px
      color: var(--vt-c-blue-text-light)
      border: none
      background-color: transparent
      &:focus
        outline: none
      &::placeholder
        color: var(--vt-c-blue-text-dark)
  .-sign-in
    position: absolute
    top: 12px
    right: 12px
    width: 120px
    height: 80px
    font-size: 18px
    font-weight: 700
    color: var(--vt-c-blue-background)
    background-color: var(--vt-c-yellow)
  .-remember-me
    position: absolute
    top: 106px
    right: 12px
.-sign-up
  float: right
</style>