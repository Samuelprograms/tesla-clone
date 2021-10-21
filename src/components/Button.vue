<template>
  <button v-on:click="printpa()">{{ text }}</button>
</template>
<script>
export default {
  name: "Button",
  props: {
    text: {
      type: String,
      required: true,
    },
  },
  methods: {
    printpa() {
      alert(this.text);
    },
  },
};
</script>
<style scoped>
button {
  width: 250px;
  height: 45px;
  border-radius: 22px;
  border: none;
  margin: 10px;
  opacity: 0.7;
  cursor: pointer;
}
@media screen and (max-width: 1000px) {
  button {
    margin: 0 0 10px 0;
  }
}
</style>
