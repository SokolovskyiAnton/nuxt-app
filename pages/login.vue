<template>
  <div>
      <form>
          <h1>Login</h1>
          <div class="form-group">
              <input type="text" class="form-control">
          </div>
          
          <p>
              <nuxt-link to="/">To home page</nuxt-link>
          </p>

          <button class="btn btn-primary">Login</button>
      </form>
  </div>
</template>

<script>
  export default {
    layout: 'auth'
  }
</script>

<style scoped>
form {
    width: 500px;
}
</style>