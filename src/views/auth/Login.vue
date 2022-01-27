<template>
  <ion-page>
    <ion-content>
      <Header type="none"/>
      <AuthTopSection title="Login to your account" paragraph="Good to see you again, enter your details below to continue ordering."/>
      <AuthForm>
        <UiInput label="Email Address" type="text" placeholder="Enter email" v-model:value="user.email"/>
        <UiInput label="Password" type="password" placeholder="Enter password" v-model:value="user.password"/>
      </AuthForm>
      <ui-actions>
        <ui-button color="background-primary-gradient" @click="login">Login to my account</ui-button>
        <ui-button color="background-white" @click="router.push('/register')">Create an account</ui-button>
      </ui-actions>
    </ion-content>
  </ion-page>
</template>

<script>
import {defineComponent, reactive} from "vue";
import {IonPage, IonContent} from "@ionic/vue";

import Header from "@/components/splashscreen/Header";
import AuthTopSection from "@/components/auth/TopSection";
import UiActions from "@/components/ui/Actions";
import UiButton from "@/components/ui/Button";
import AuthForm from "@/components/auth/Form";
import UiInput from "@/components/ui/Input";
import {useRouter} from "vue-router";

export default defineComponent({
  name: "AuthLogin",
  components: {UiInput, AuthForm, UiButton, UiActions, AuthTopSection, IonPage, IonContent, Header},
  setup() {
    const router = useRouter()

    const user = reactive({
      email: "",
      password: ""
    })

    const login = () => {
      console.log(user.email)
      console.log(user.password)

      router.push('/home')
    }

    return {router, user, login}
  }
})
</script>