<template>
<div>
  <b-navbar type="dark" variant="info">
    <b-navbar-brand to="/">Nuxt</b-navbar-brand>
     <b-navbar-nav>

        <nuxt-link tag="li" to="/" class="nav-item" exact active-class="active">
            <a class="nav-link">Home</a>
        </nuxt-link>

        <nuxt-link tag="li" to="/about" class="nav-item" active-class="active" no-prefetch>
            <a class="nav-link">About</a>
        </nuxt-link>

        <nuxt-link tag="li" to="/users" class="nav-item" active-class="active" no-prefetch>
            <a class="nav-link">Users</a>
        </nuxt-link>
        
        <nuxt-link tag="li" to="/login" class="nav-item" active-class="active" no-prefetch>
            <a class="nav-link">Login</a>
        </nuxt-link>

      </b-navbar-nav>
  </b-navbar>
</div>
</template>

<script>
  export default {
    data() {
      return {
      }
    }
  }
</script>

<style scoped>
</style>