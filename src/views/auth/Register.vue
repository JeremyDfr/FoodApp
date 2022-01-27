<template>
  <ion-page>
    <ion-content>
      <Header type="none"/>
      <AuthTopSection title="Create an account" paragraph="Welcome friend, enter your details so lets get started in ordering food."/>
      <AuthForm>
        <UiInput label="Email Address" type="text" placeholder="Enter email" v-model:value="user.email"/>
        <UiInput label="Password" type="password" placeholder="Enter password" v-model:value="user.password"/>
        <UiInput label="Confirm Password" type="password" placeholder="Confirm password" v-model:value="user.confirmPassword"/>
      </AuthForm>
      <ui-actions>
        <ui-button color="background-primary-gradient" @click="register">Create an account</ui-button>
        <ui-button color="background-white" @click="router.push('/login')">Login to my account</ui-button>
      </ui-actions>
    </ion-content>
  </ion-page>
</template>

<script>
import {defineComponent, reactive} from "vue";
import {IonPage, IonContent} from "@ionic/vue";

import Header from "@/components/splashscreen/Header";
import UiActions from "@/components/ui/Actions";
import UiButton from "@/components/ui/Button";
import {useRouter} from "vue-router";
import UiInput from "@/components/ui/Input";
import AuthTopSection from "@/components/auth/TopSection";
import AuthForm from "@/components/auth/Form";

export default defineComponent({
  name: "AuthRegister",
  components: {AuthForm, AuthTopSection, UiInput, UiButton, UiActions, IonPage, IonContent, Header},
  setup() {
    const router = useRouter()
    const user = reactive({
      email: "",
      password: "",
      confirmPassword: ""
    })

    const register = () => {
      console.log(user.email)
      console.log(user.password)
      console.log(user.confirmPassword)
    }

    return {router, user, register}
  }
})
</script>