<template>
  <header v-on:click="changeTitle">
    <h2>{{msg}}</h2>
  </header>
</template>

<script>
export default {
  name: "Header",
  data () {
    return {
      msg: '这是一个标题'
    }
  },
  methods: {
    changeTitle (event) {
      this.$emit('toChange', '子向父组件传值', event);
    }
  }
}
</script>

<style scoped>
header {
  width: 100%;
  max-width: 1200px;
  margin: 0 auto;
  background-color: lightseagreen;
  padding: 30px 0 30px 0;
}

header h2 {
  text-align: center;
  color: #CCC;
}

</style>
