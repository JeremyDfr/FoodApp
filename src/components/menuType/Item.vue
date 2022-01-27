<template>
  <div class="menu__type__item">
    <div>
      <img :src="item.img" alt="">
      <p>{{ item.name }}</p>
    </div>
  </div>
</template>

<script>
import {defineComponent} from "vue";

export default defineComponent({
  name: "MenuTypeItem",
  props: {
    item: {}
  }
})
</script>