<template>
  <div>
    {{ msg }}
    <app-header
      v-bind:propsMsg="msg"
      propsMsg2="msg"
      v-on:renew="reNewMsg"
    ></app-header>
  </div>
</template>

<script>
import AppHeader from "./components/AppHeader.vue";

export default {
  data: function () {
    return {
      msg: "hi",
    };
  },
  components: {
    "app-header": AppHeader,
  },
  methods: {
    reNewMsg: function () {
      this.msg = "renew String";
    },
  },
};
</script>

<style></style>
