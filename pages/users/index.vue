<template>
  <div>
      <h1>Users page</h1>
      <ul>
          <li v-for="user of users" :key="user.id">
              <a href="#" @click.prevent="toUser(user.id)">{{user.name}}</a>
          </li>
      </ul>
  </div>
</template>

<script>
  export default {
    async fetch({store}) {
      if (store.getters['users/users'].length === 0) {
        await store.dispatch('users/fetch')
      }
    },
    computed: {
      users() {
        return this.$store.getters['users/users']
      }
    },
    methods: {
        toUser(user) {
            this.$router.push('/users/' + user)
        }
    }
  }
</script>

<style scoped>
</style>