<template>
  <header class="header">
    <nav class="nav">
      <img src="/assets/logo.png" alt="tesla logo" />
      <ul class="center">
        <li><a href="">Model S</a></li>
        <li><a href="">Model 3</a></li>
        <li><a href="">Model X</a></li>
        <li><a href="">Model Y</a></li>
        <li><a href="">Solar Roof</a></li>
        <li><a href="">Solar Panels</a></li>
      </ul>
      <ul class="end">
        <li><a href="">Shop</a></li>
        <li><a href="">Account</a></li>
        <li><a href="">Menu</a></li>
      </ul>
    </nav>
  </header>
</template>

<script>
export default {
  name: "Header",
};
</script>
<style scoped>
.header {
  z-index: 20;
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
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
  transition: all 0.3s ease-in-out;
}
.nav ul li:hover {
  background: rgba(100, 100, 100, 0.1);
}
.nav ul li a {
  color: #111;
  font-weight: 400;
  text-decoration: none;
  font-size: 14px;
  width: 100%;
  height: 100%;
}
</style>
