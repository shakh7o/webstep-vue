<script setup>
import myHeader from "./components/app/myHeader.vue";
import myFooter from "./components/app/myFooter.vue";
</script>

<template>
  <div>
    <my-header />
    <main class="main">
      <RouterView />
    </main>
    <myFooter />
  </div>
</template>

<style lang="scss" scoped>
</style>
