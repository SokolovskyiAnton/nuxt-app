<template>
  <div>
      <h2 class="mt-3">{{user.name}}</h2>
      <hr>
      <p>{{user.email}}</p>
  </div>
</template>

<script>
  export default {
    data() {
      return {
      }
    },
    validate({params}) {
      return /^\d+$/.test(params.id)
    },
    async asyncData({$axios, params}) {
      const user = await $axios.$get('https://jsonplaceholder.typicode.com/users/' + params.id)
      return {user}
    }
  }
</script>

<style scoped>
</style>