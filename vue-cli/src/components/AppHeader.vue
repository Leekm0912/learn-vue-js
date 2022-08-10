<template>
  <header>
    <h1>Header</h1>
    <p>props : {{ propsMsg }}</p>
    <p>props : {{ propsMsg2 }}</p>
    <button v-on:click="sendEvent">send</button>
  </header>
</template>

<script>
export default {
  props: {
    propsMsg: String,
    propsMsg2: String,
  },
  methods: {
    sendEvent: function () {
      console.log("sendEvent");
      this.$emit("renew");
    },
  },
};
</script>

<style></style>
