<template>
  <form v-on:submit.prevent="submitForm">
    <div>
      <label for="username">id : </label>
      <input id="username" type="text" v-model="username" />
    </div>
    <div>
      <label for="password">pw : </label>
      <input id="password" type="password" v-model="password" />
    </div>
    <button>login</button>
  </form>
</template>

<script>
// import axios
import axios from "axios";

export default {
  data: function () {
    return {
      username: null,
      password: null,
    };
  },
  methods: {
    submitForm: function () {
      // event.preventDefault();
      console.log(this.username, this.password);
      var url = "https://jsonplaceholder.typicode.com/users";
      var data = {
        username: this.username,
        password: this.password,
      };
      axios
        .post(url, data)
        .then(function (res) {
          console.log(res);
        })
        .catch(function (e) {
          console.log(e);
        });
    },
  },
};
</script>

<style></style>
