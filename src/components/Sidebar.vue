<template>
  <div class="container">
    <div class="sidebar">
      <button @click="$emit('close-sidebar')">x</button>
      <ul class="sidebar__items">
        <div class="responsive-links">
          <li class="sidebar__item" @click="$emit('close-sidebar')">
            <a href="#model-s">Model S</a>
          </li>
          <li class="sidebar__item" @click="$emit('close-sidebar')">
            <a href="#model-3">Model 3</a>
          </li>
          <li class="sidebar__item" @click="$emit('close-sidebar')">
            <a href="#model-x">Model X</a>
          </li>
          <li class="sidebar__item" @click="$emit('close-sidebar')">
            <a href="#model-y">Model Y</a>
          </li>
          <li class="sidebar__item" @click="$emit('close-sidebar')">
            <a href="#solar-roof">Solar Roof</a>
          </li>
          <li class="sidebar__item" @click="$emit('close-sidebar')">
            <a href="#solar-panels">Solar Panels</a>
          </li>
          <li class="sidebar__item" @click="$emit('close-sidebar')">
            <a href="">Account</a>
          </li>
          <li class="sidebar__item" @click="$emit('close-sidebar')">
            <a href="">Shop</a>
          </li>
        </div>
        <li
          :key="item"
          v-for="item in sidebarItems"
          class="sidebar__item"
          @click="$emit('close-sidebar')"
        >
          <a href="">{{ item }}</a>
        </li>
      </ul>
    </div>
  </div>
</template>
<script>
export default {
  name: "Sidebar",
  data() {
    return {
      sidebarItems: [
        "Existing Inventory",
        "Used Inventory",
        "Trade-In",
        "Test Drive",
        "Cybertruck",
        "Roadster",
        "Semi",
        "Charging",
        "Powerwall",
        "Commercial Energy",
        "Utilities",
        "Find Us",
        "Support",
        "Investor Relations",
      ],
    };
  },
};
</script>
<style scoped>
.container {
  position: fixed;
  z-index: 100;
  top: 0;
  left: 0;
  width: 100%;
  height: 100vh;
  display: flex;
  flex-direction: column;
  align-items: flex-end;
  backdrop-filter: blur(4px);
}
.sidebar {
  text-align: end;
  background: #fff;
  padding: 40px;
  height: 100%;
  width: 320px;
  overflow-y: scroll;
}
button {
  padding: 5px 15px;
  border: none;
  background: transparent;
  border-radius: 50%;
  font-size: 20px;
}
button:hover {
  cursor: pointer;
  background: #eee;
}
.sidebar__items {
  text-align: start;
  width: 100%;
}
.sidebar__item {
  list-style: none;
  width: 100%;
  cursor: pointer;
  border-radius: 15px;
  padding: 7px 15px;
  margin: 10px 0;
}
.sidebar__item:hover {
  background: #eee;
}
.sidebar__item a {
  text-decoration: none;
  color: #111;
}
.responsive-links {
  display: none;
}
@media screen and (max-width: 1000px) {
  .responsive-links {
    display: inherit;
  }
}
</style>
