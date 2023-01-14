<template>
  <Form v-slot="{ values }" @submit="onSubmit" :validation-schema="schema" :initial-values="formValues">
    <div class="mb-3">
      <label for="username" class="form-label">Email</label>
      <Field id="username" name="username" class="form-control" type="email" />
    </div>
    <div class="mb-3">
      <label for="password" class="form-label">Senha</label>
      <Field name="password" class="form-control" type="password" />
    </div>
    <pre>{{ values }}</pre>
    <div class="d-grid gap-2 mb-3">
      <button class="btn btn-primary" type="submit">Login</button>
    </div>
  </Form>
</template>

<script lang="ts">
import {Field, Form} from 'vee-validate'
import * as yup from 'yup';
import {defineComponent} from "vue"

const schema = yup.object({
  username: yup.string().required().email(),
  password: yup.string().required().min(8),
});

const formValues = {
  username: '',
  password: '',
}

export default defineComponent({
  name: 'LoginForm',
  components: {
    Form,
    Field,
  },
  data() {
    return {
      schema : schema,
      formValues: formValues,
    }
  },
  methods:{
    onSubmit( values : any ){
      console.log( JSON.stringify( values ) )
    }
  }
})
</script>

<style scoped>

</style>
