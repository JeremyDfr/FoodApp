<template>
  <div class="actions">
    <slot></slot>
  </div>
</template>

<script>
import {defineComponent} from "vue";

export default defineComponent({
  name: "UiActions",
})
</script>

<style lang="scss">
div.actions {
  margin: 20px 20px 0;
  text-align: center;

  button:last-child {
    margin-top: 20px;
  }
}
</style>