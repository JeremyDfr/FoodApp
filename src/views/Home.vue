<template>
  <ion-page>
    <ion-content id="home">
      <h1>Enjoy Delicious food</h1>
      <menu-type-list></menu-type-list>
    </ion-content>
  </ion-page>
</template>

<script>
import { IonContent, IonPage } from '@ionic/vue';
import { defineComponent } from 'vue';
import MenuTypeList from "@/components/menuType/List";

export default defineComponent({
  name: "HomePage",
  components: {
    MenuTypeList,
    IonContent,
    IonPage,
  }
});
</script>

<style lang="scss">
#home {
  h1 {
    margin: 40px 20px 0;
  }

  .menu__type__list {
    margin-top: 50px;
  }
}
</style>