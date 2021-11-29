<template>
  <img alt="Vue logo" src="./assets/logo.png" />
  <HelloWorld msg="Vue Tutorial" name="k-yama" />
  <UserInfo name="山田 太郎" age="25" />
  <GetUsers />

  <!-- <Button buttonText="テストボタン" /> -->
  <div>
    <button @click="count++">increment</button>
    <button @click="count--">decrement</button>
    <p>{{ count }}</p>
  </div>
  <div>
    <div v-for="user in users" :key="user.id">
      <p>{{ user.name }}</p>
      <p>{{ user.age }}</p>
    </div>
  </div>
</template>

<script>
import GetUsers from "./components/GetUsers.vue";
// import Button from './components/Button.vue'
import HelloWorld from "./components/HelloWorld.vue";
import UserInfo from "./components/UserInfo.vue";

export default {
  name: "App",
  components: {
    HelloWorld,
    UserInfo,
    GetUsers,
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
};
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
