<template>
  <form>

    <div class="mb-3">
      <label for="username" class="form-label">Email</label>
      <input type="email" class="form-control" id="username" placeholder="email@example.com">
    </div>
    <div class="mb-3">
      <label for="password" class="form-label">Senha</label>
      <input type="text" class="form-control" id="password">
    </div>
    <div class="mb-3">
      <div class="d-grid gap-2">
        <button class="btn btn-primary" type="button">Login</button>
      </div>
    </div>

  </form>
</template>

<script lang="ts">
import {defineComponent} from "vue";

export default defineComponent({
  name: 'LoginForm',
  data() {
    return {
      message: "Mensagem"
    }
  }
});

</script>

<style scoped>

</style>
