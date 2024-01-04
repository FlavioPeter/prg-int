<template>
  <nav class="navbar">

      <div class="logo">
        <img src="../assets/company-logo2.jpg" alt="Product Logo" />
      </div>
      <ul class="nav">
        <li><RouterLink to="/">Home</RouterLink></li>
        <li><RouterLink to="/about">About</RouterLink></li>
        <li><RouterLink to="/products">Products</RouterLink></li>
        <li><RouterLink to="/contact">Contact</RouterLink></li>
      </ul>

  </nav>
</template>

<script setup>
import { RouterLink } from "vue-router";
</script>

<style scoped>
ul {
  list-style: none;
}

.navbar {
  background: #3474e6;
  display: flex;
  color: #fff;
  height: 60px;
  justify-content: space-between;
  align-items: center;
}

.navbar .logo {
  font-size: x-large;
  font-weight: bold;
  margin-left: 10px;
  min-width: 55px;
}

.navbar img {
  margin: auto;
  height: 65px;
  position: center;
}

.navbar a {
  color: #fff;
  text-decoration: none;
  font-size: 18px;
  font-weight: bold;
}

.navbar a:hover {
  color: lightblue;
}

.navbar ul {
  display: flex;
}

.navbar ul li {
  margin: 20px;
}
</style>