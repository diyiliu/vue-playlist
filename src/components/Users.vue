<template>
  <div class="users">
    <h1>{{ appTitle }}</h1>
    <ul>
      <li v-for="user in users">
        <h3>{{ user.name }}</h3>
        <p >{{user.email}}</p>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: "Users",
  props:{
    appTitle:{
      type: String
    },
    users: {
      type: Array,
      required: true
    }
  },
  data () {
    return {

    }
  }
}
</script>

<style scoped>
.users {
  width: 100%;
  max-width: 1200px;
  box-sizing: border-box;
  margin: 0 auto;
  padding: 20px;
}

h1{
  margin-bottom: 20px;
}

ul {
  display: flex;
  flex-wrap: wrap;
  list-style-type: none;
  padding: 0;
}

li {
  flex-grow: 1;
  flex-basis: 200px;
  text-align: center;
  padding: 30px;
  border: 1px solid #333;
  margin: 10px;
}
</style>
