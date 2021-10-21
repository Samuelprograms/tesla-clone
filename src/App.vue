<template>
  <div>
    <Header
      v-on:open-sidebar="
        () => {
          this.showSidebar = true;
        }
      "
    />
    <Panel
      id="model-s"
      title="Model S"
      text="Order Online for Touchless Delivery"
      image="model-s.jpg"
      twoButtons
    />
    <Panel
      id="model-3"
      title="Model 3"
      text="Order Online for Touchless Delivery"
      image="model-3.jpg"
      twoButtons
    />
    <Panel
      id="model-x"
      title="Model X"
      text="Order Online for Touchless Delivery"
      image="model-x.jpg"
      twoButtons
    />
    <Panel
      id="model-y"
      title="Model Y"
      text="Order Online for Touchless Delivery"
      image="model-y.jpg"
      twoButtons
    />
    <Panel
      id="solar-roof"
      title="Solar Roof"
      text="Produce Clean Energy From Your Roof"
      image="solar-roof.jpg"
      twoButtons
    />
    <Panel
      id="solar-panels"
      title="Solar Panels"
      text="Lowest Cost Solar Panels in America"
      image="solar-panel.jpg"
      twoButtons
    />
    <Panel title="Accesories" image="accesories.jpg" />
    <Sidebar
      title="Accesories"
      v-if="showSidebar"
      v-on:close-sidebar="
        () => {
          this.showSidebar = false;
        }
      "
    />
  </div>
</template>

<script>
import Header from "./components/Header.vue";
import Panel from "./components/Panel.vue";
import Sidebar from "./components/Sidebar.vue";
export default {
  name: "App",
  components: {
    Header,
    Panel,
    Sidebar,
  },
  data() {
    return {
      showSidebar: false,
    };
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
  transition: all 0.3s ease-in-out;
}
</style>
