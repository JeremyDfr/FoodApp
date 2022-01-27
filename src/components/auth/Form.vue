<template>
  <form class="auth__form">
    <slot></slot>
  </form>
</template>

<script>
import {defineComponent} from "vue";

export default defineComponent({
  name: "AuthForm"
})
</script>

<style lang="scss">
form.auth__form {
  margin: 50px 20px 80px 20px;
}
</style>