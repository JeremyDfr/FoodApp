<template>
  <div class="form-control">
    <ion-label>{{ label }}</ion-label>
    <ion-input class="custom" :type="type" :placeholder="placeholder" :value="value" @input="$emit('update:value', $event.target.value)"></ion-input>
  </div>
</template>

<script>
import {defineComponent} from "vue";
import {IonLabel, IonInput} from "@ionic/vue";

export default defineComponent({
  name: "UiInput",
  components: {IonLabel, IonInput},
  props: {
    label: String,
    type: String,
    placeholder: String,
    value: String
  },
  setup(props, context) {

    const sendData = (data) => {
      context.emit('inputCustom', data)
    }

    return {sendData}
  }
})
</script>

<style lang="scss">
div.form-control {
  &:not(:first-child) {
    margin-top: 20px;
  }

  ion-label {
    margin-left: 20px;
  }

  ion-input.custom {
    --background: #fff;
    border-radius: 15px;
    padding: 15px 20px;
    --padding-bottom: 15px;
    --padding-top: 15px;
    --padding-start: 20px;
    --padding-end: 20px;
    margin-top: 10px;
  }
}
</style>