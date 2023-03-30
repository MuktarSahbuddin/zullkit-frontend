<script setup>
import { RouterLink, RouterView } from "vue-router";
import NavbarComponents from "./components/layouts/NavbarComponents.vue";
</script>

<template>
  <NavbarComponents />
  <RouterView />
</template>

<style>
@import "@/assets/css/styles.css";
</style>