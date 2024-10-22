<template>
  <nav class="p-5 bg-green-400 text-white mb-10">
    <router-link :to="{ name: 'Home' }">Just To Test Plesk</router-link>
  </nav>
  <div class="container">
    <router-view></router-view>
    <div v-if="isLoading" >Loading...</div>
  </div>
</template>

<script setup>
import usePageRequests from './composables/usePageRequests'
const {isLoading} = usePageRequests()
</script>
<style lang="css">
.container {
  max-width: 960px;
  margin: 0 auto;
}
</style>
