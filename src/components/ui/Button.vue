<template>
  <button :class="color">
    <slot></slot>
  </button>
</template>

<script>
import {defineComponent} from "vue";

export default defineComponent({
  name: "UiButton",
  props: {
    color: null
  },
})
</script>

<style lang="scss">
button {
  width: 100%;
  border-radius: 20px;
  padding: 20px;
  font-size: 15px;
  font-weight: bold;
  box-shadow: 5px 5px 5px rgb(0 0 0 / 5%);

  &.background-white {
    background: #FFFFFF;
    color: #F9881F;
  }

  &.background-primary-gradient {
    background: #F9881F;
    color: #FFFFFF;
  }
}
</style>