<template>
  <div id="home">
    <app-header v-on:toChange="doChange"></app-header>
    <app-users v-bind:appTitle="title" v-bind:users="users"></app-users>
    <app-footer></app-footer>
  </div>
</template>

<script>

import Header from './layout/Header'
import Footer from './layout/Footer'
import Users from './Users'

export default {
  name: 'home',
  components: {
    'app-header': Header,
    'app-footer': Footer,
    'app-users': Users
  },
  data () {
    return {
      title: '来自父级的标题',
      users: []
    }
  },
  methods: {
    doChange (title, $event) {
      this.title = title;
      console.log($event);
    }
  },
  created(){
    this.$http.get('https://jsonplaceholder.typicode.com/users')
      .then(data => {
        this.users = data.body;
      })
  }
}
</script>

<style scoped>

</style>
