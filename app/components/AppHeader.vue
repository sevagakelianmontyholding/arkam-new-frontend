<template>
  <header class="h-(--header-height) absolute top-0 w-full z-10 bg-background">
    <div class="container h-full flex justify-between items-center">
      <Logo />
      <Hamburger />
    </div>
  </header>
</template>

<script setup>
import Hamburger from "./Hamburger.vue";
</script>

<style lang="scss" scoped></style>
