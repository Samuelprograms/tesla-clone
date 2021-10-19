<template>
  <div
    :style="{ backgroundImage: `url(/assets/${image})` }"
    class="panel background"
  >
    <div style="text-align: center">
      <h1>{{ title }}</h1>
      <p>{{ text }}</p>
    </div>
    <div>
      <Button text="click me" />
      <Button v-if="twoButtons" text="existing inventory" />
    </div>
  </div>
</template>
<script>
import Button from "./Button.vue";
export default {
  name: "Panel",
  props: {
    title: {
      type: String,
      required: true,
    },
    image: {
      type: String,
      required: true,
    },
    text: String,
    twoButtons: Boolean,
  },
  components: {
    Button,
  },
};
</script>
<style scope>
.panel {
  position: relative;
  display: flex;
  flex-direction: column;
  justify-content: space-around;
  align-items: center;
  background-position: center center;
  background-size: cover;
  background-repeat: no-repeat;
  z-index: 10;
  width: 100%;
  height: 100vh;
}
</style>
