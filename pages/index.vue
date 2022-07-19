<template>
  <section>
    <h3>VeeValidate - Nuxt Example:</h3>
    <ValidationProvider rules="required|alpha" v-slot="{ errors }">
      <input type="text" v-model="value">
      <span>{{ errors[0] }}</span>
    </ValidationProvider>
  </section>
</template>

<script>
import { ValidationProvider } from "vee-validate";

export default {
  components: {
    ValidationProvider
  },
  data: () => ({
    value: ""
  })
};
</script>
