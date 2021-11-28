<template>
  <img alt="Vue logo" src="./assets/logo.png">
  <HelloWorld msg="Vue Tutorial" name="k-yama"/>
  <UserInfo name="山田 太郎" age=25 />
  <!-- <Button buttonText="テストボタン" /> -->
  <div>
    <button @click="count++">increment</button>
    <button @click="count--">decrement</button>
    <p>{{ count }}</p>
  </div>
</template>

<script>
// import Button from './components/Button.vue'
import HelloWorld from './components/HelloWorld.vue'
import UserInfo from './components/UserInfo.vue'

export default {
  name: 'App',
  components: {
    HelloWorld,
    UserInfo,
    // Button
  },
  data() {
    return { count: 0 };
  },
  methods: {
    increment() {
      this.count++;
    },
    decrement() {
      this.count--;
    },
  },
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
