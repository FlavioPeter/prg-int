<template>
  <header>
    <NavComp />
  </header>

  <RouterView />
</template>

<script setup>
import { RouterView } from "vue-router";
import NavComp from "./components/NavComp.vue";
</script>

<style>
</style>
