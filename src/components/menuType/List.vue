<template>
  <div class="menu__type__list">
    <menu-type-item v-for="item in list" :key="item" :item="item"></menu-type-item>
  </div>
</template>

<script>
import {defineComponent} from "vue";
import MenuTypeItem from "@/components/menuType/Item";

export default defineComponent({
  name: "MenuTypeList",
  components: {MenuTypeItem},
  setup() {
    const list = [
      {
        img: "assets/images/menuType/img_1.png",
        name: "Pizza"
      },
      {
        img: "assets/images/menuType/img_1.png",
        name: "Sausage"
      },
      {
        img: "assets/images/menuType/img_1.png",
        name: "Burger"
      },
      {
        img: "assets/images/menuType/img_1.png",
        name: "Samosa"
      },
    ]

    return {list}
  }
})
</script>

<style lang="scss">
.menu__type__list {
  display: flex;
  overflow-x: scroll;

  &::-webkit-scrollbar {
    display: none;
  }

  .menu__type__item {
    min-width: 80px;
    display: flex;
    min-height: 110px;
    justify-content: center;
    align-items: center;
    border: 1px solid rgb(169 232 139 / 70%);
    border-radius: 50px;
    margin-left: 30px;

    > div {
      min-width: 60px;
      min-height: 90px;
      display: flex;
      flex-direction: column;
      justify-content: center;
      align-items: center;
      background: rgba(169, 232, 139, 0.2);
      border-radius: 50px;

      img {
        width: 27px;
        height: 27px;
      }

      p {
        font-size: 12px;
        margin: 15px 0 0;
      }
    }
  }
}
</style>