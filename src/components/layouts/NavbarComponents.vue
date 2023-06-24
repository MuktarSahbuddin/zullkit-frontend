<script setup>
import { onMounted, computed } from 'vue'
import { useUserStore } from '@/stores/user'

import LogoComponents from "./LogoComponents.vue";
import NavigationLinks from "./NavigationLinks.vue";
import UserInfo from "./UserInfo.vue";
import AuthBotton from "./AuthBotton.vue";

const userStore = useUserStore()
const user = computed(() => userStore.getUser)
const isLoggedIn = computed(() => userStore.isLoggedIn)

onMounted(() => {
  userStore.fetchUser()
})

</script>


<template>
  <nav
    class="bg-white border-gray-200 px-2 sm:px-4 py-2.5 rounded dark:bg-gray-800"
  >
    <div
      class="container flex flex-wrap items-center justify-between mx-auto my-2"
    >
      <LogoComponents />
      <UserInfo v-if="isLoggedIn" :user="user.data"/>
      <AuthBotton v-else/>
      <NavigationLinks />
    </div>
  </nav>
</template>

