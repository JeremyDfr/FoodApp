<template>
  <ion-header class="ion-no-border">
    <img src="../../../public/assets/images/splashscreen/logo-small.png" alt="">
    <router-link class="text-orange" to="/register" v-if="type == 'skip'">Skip</router-link>
    <router-link class="text-orange" to="/login" v-if="type == 'cancel'">Cancel</router-link>
  </ion-header>
</template>

<script>
import {defineComponent} from "vue";
import {IonHeader} from "@ionic/vue";

export default defineComponent({
  name: "SplashscreenHeader",
  components: {
    IonHeader
  },
  props: {
    type: {
      type: String,
      default: 'skip'
    }
  }
})
</script>

<style lang="scss">
ion-header {
  position: relative;
  display: flex;
  justify-content: center;
  align-items: center;
  padding: 20px 0px;

  img {
    width: 34px;
    height: auto;
  }

  a {
    position: absolute;
    right: 20px;
    text-decoration: none;
  }
}
</style>