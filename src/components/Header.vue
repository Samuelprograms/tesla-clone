<template>
  <header class="header">
    <nav class="nav">
      <img src="/assets/logo.png" alt="tesla logo" />
      <ul class="center">
        <li><a href="#model-s">Model S</a></li>
        <li><a href="#model-3">Model 3</a></li>
        <li><a href="#model-x">Model X</a></li>
        <li><a href="#model-y">Model Y</a></li>
        <li><a href="#solar-roof">Solar Roof</a></li>
        <li><a href="#solar-panels">Solar Panels</a></li>
      </ul>
      <ul class="end">
        <li class="extra-link"><a href="">Shop</a></li>
        <li class="extra-link"><a href="">Account</a></li>
        <li @click="$emit('open-sidebar')">Menu</li>
      </ul>
    </nav>
  </header>
</template>

<script>
export default {
  name: "Header",
  methods: {},
  data() {},
};
</script>
<style scoped>
.header {
  z-index: 20;
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  padding: 0 15px;
}
.nav {
  height: 50px;
  display: flex;
  justify-content: space-between;
  align-items: center;
}
.nav img {
  width: 150px;
}
.nav ul {
  display: flex;
  justify-content: center;
  align-items: center;
}
.center {
  width: 580px;
}
.end {
  width: 200px;
}
.nav ul li {
  list-style: none;
  border-radius: 10px;
  padding: 5px 15px;
}
.nav ul li:hover {
  background: rgba(100, 100, 100, 0.1);
}
.nav ul li a {
  color: #111;
  font-weight: 400;
  text-decoration: none;
  font-size: 14px;
}
@media screen and (max-width: 1000px) {
  .nav ul {
    flex-direction: column;
  }
  .center,
  .center li,
  .center li a {
    display: none;
  }
  .extra-link {
    display: none;
  }
}
</style>
