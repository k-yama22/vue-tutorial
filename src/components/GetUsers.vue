<template>
  <div>
    <div>ユーザー情報をaxiosで取得</div>
    <div v-for="user in users" :key="user.id">
      <p>{{ user.name }}</p>
      <p>{{ user.age }}</p>
    </div>
    <br />
  </div>
</template>

<script>
import axios from "axios";
export default {
  name: "GetUsers",
  data() {
    return {
      users: [],
    };
  },
  created() {
    this.getUsers();
  },
  methods: {
    getUsers: function () {
      axios
        .get("http://localhost:3000/users")
        .then((res) => {
          console.log(res);
          this.users = res.data;
        })
        .catch((err) => {
          console.log(err);
        });
    },
  },
};
</script>
