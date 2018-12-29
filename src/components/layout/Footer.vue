<template>
  <footer>
    <p>{{msg}}</p>
  </footer>
</template>

<script>
export default {
  name: "Header",
  data () {
    return {
      msg: '@copyright 2018'
    }
  }
}
</script>

<style scoped>
footer{
  width: 100%;
  max-width: 1200px;
  margin: 0 auto;
  background-color: #CCC;
  padding: 30px 0 30px 0;
}

footer p{
  text-align: center;
  color: lightseagreen;
}

</style>
