<template>
  <ion-page>
    <ion-content class="layout__base">
      <Header/>
      <ion-slides pager="true" :options="slideOpts">
        <ion-slide>
          <h1>Order from your favourite stores or vendors</h1>
          <img src="../../../public/assets/images/splashscreen/slide-one.png" alt="">
        </ion-slide>
        <ion-slide>
          <h1>Choose from a wide range of delicious meals</h1>
          <img src="../../../public/assets/images/splashscreen/slide-two.png" alt="">
        </ion-slide>
        <ion-slide>
          <h1>Enjoy instant delivery and payment</h1>
          <img src="../../../public/assets/images/splashscreen/slide-three.png" alt="">
        </ion-slide>
      </ion-slides>
      <ui-actions>
        <ui-button color="background-primary-gradient" @click="register">Create an account</ui-button>
        <ui-button color="background-white" @click="login">Login</ui-button>
      </ui-actions>
    </ion-content>
  </ion-page>
</template>

<script>
import {defineComponent} from "vue";
import {IonPage, IonContent, IonSlides, IonSlide} from "@ionic/vue";
import {useRouter} from "vue-router"

import Header from "@/components/splashscreen/Header";
import UiButton from "@/components/ui/Button"
import UiActions from "@/components/ui/Actions";

export default defineComponent({
  name: "SplashscreenPage",
  components: {
    UiActions,
    UiButton,
    IonPage,
    IonContent,
    Header,
    IonSlides,
    IonSlide
  },
  setup() {
    const router = useRouter()

    const register = () => {
      router.push('/register')
    }

    const login = () => {
      router.push('/login')
    }

    const slideOpts = {
      initialSlide: 0,
      speed: 400
    };
    return {slideOpts, register, login}
  }
})
</script>

<style lang="scss">
ion-slides.slides-md, ion-slides.slides-ios {
  --bullet-background-active: #0B735F;

  ion-slide {
    display: flex;
    flex-direction: column;
    padding: 0 20px;

    h1 {
      margin-top: 40px;
    }

    img {
      margin-top: 40px;
    }
  }

  ion-slide:last-child img {
    width: 80%;
  }
}
</style>