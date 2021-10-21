<template>
  <div
    :style="{ backgroundImage: `url(/assets/${image})` }"
    class="panel background"
  >
    <div style="text-align: center">
      <h1>{{ title }}</h1>
      <p>{{ text }}</p>
    </div>
    <div class="buttons">
      <Button text="click me" style=" background:black; color:white" />
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
<style scoped>
.panel {
  position: relative;
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  align-items: center;
  background-position: center center;
  background-size: cover;
  background-repeat: no-repeat;
  z-index: 10;
  width: 100%;
  height: 100vh;
  padding: 100px 0;
}
.panel:last-child {
  background-size: contain;
}
@media screen and (max-width: 1000px) {
  .buttons {
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
  }
}
</style>
