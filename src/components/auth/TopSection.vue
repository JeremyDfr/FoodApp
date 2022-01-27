<template>
  <section class="auth__top__section">
    <h1>{{ title }}</h1>
    <p>{{ paragraph }}</p>
  </section>
</template>

<script>
import {defineComponent} from "vue";

export default defineComponent({
  name: "AuthTopSection",
  props: {
    title: String,
    paragraph: String
  }
})
</script>

<style lang="scss">
section.auth__top__section {
  margin: 0 45px;
}
</style>