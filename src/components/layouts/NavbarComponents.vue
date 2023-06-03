<script setup>
import LogoComponents from "./LogoComponents.vue";
import NavigationLinks from "./NavigationLinks.vue";
import UserInfo from "./UserInfo.vue";
import AuthBotton from "./AuthBotton.vue";
</script>


<template>
  <nav
    class="bg-white border-gray-200 px-2 sm:px-4 py-2.5 rounded dark:bg-gray-800"
  >
    <div
      class="container flex flex-wrap items-center justify-between mx-auto my-2"
    >
      <LogoComponents />
      <NavigationLinks />
      <UserInfo />
      <!-- <AuthBotton /> -->
    </div>
  </nav>
</template>

