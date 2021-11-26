<template>
  <div class="user">
    <h1>ユーザ情報</h1>
    <div class="name">{{ name }}</div>
    <div>{{ age }}</div>
  </div>
</template>

<script>
export default {
  name: 'UserInfo',
  props: {
    name: String,
    age: Number
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

.name {
  color: #42b983;
}
</style>
