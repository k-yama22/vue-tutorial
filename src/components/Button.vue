<template>
  <button>
    {{buttonText}}
  </button>
</template>

<script>
export default {
  name: 'Button',
  props: {
    buttonText: String
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

button {
  background-color: #42b983;
}
</style>
