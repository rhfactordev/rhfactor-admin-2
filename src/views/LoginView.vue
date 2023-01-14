<template>
  <div class="container">
    <div class="row">
      <div class="col-12 col-md-8 offset-md-2 col-lg-6 offset-lg-3">
        <login-form />
      </div>
    </div>

  </div>

</template>

<script lang="ts">
import {defineComponent} from 'vue';
import LoginForm from "@/components/LoginForm.vue";

export default defineComponent({
  name: 'LoginView',
  components: {LoginForm},
});
</script>
