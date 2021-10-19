<template>
  <div>
    <Header />
    <Panel
      title="Model S"
      text="Order Online for Touchless Delivery"
      image="model-s.jpg"
      twoButtons
    />
    <Panel
      title="Model 3"
      text="Order Online for Touchless Delivery"
      image="model-3.jpg"
      twoButtons
    />
    <Panel
      title="Model X"
      text="Order Online for Touchless Delivery"
      image="model-x.jpg"
      twoButtons
    />
    <Panel
      title="Model Y"
      text="Order Online for Touchless Delivery"
      image="model-y.jpg"
      twoButtons
    />
    <Panel
      title="Solar Roof"
      text="Produce Clean Energy From Your Roof"
      twoButtons
    />
    <Panel
      title="Solar Panels"
      text="Lowest Cost Solar Panels in America"
      twoButtons
    />
    <Panel title="Accesories" />
  </div>
</template>

<script>
import Header from "./components/Header.vue";
import Panel from "./components/Panel.vue";
export default {
  name: "App",
  components: {
    Header,
    Panel,
  },
};
</script>
<style>
@import url("https://fonts.googleapis.com/css2?family=Sawarabi+Gothic&display=swap");
* {
  font-family: "Sawarabi Gothic", sans-serif;
  box-sizing: border-box;
  margin: 0;
  padding: 0;
}
</style>
