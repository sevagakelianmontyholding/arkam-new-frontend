<template>
  <div>
    <AppHeader @toggle-menu="isMenuOpen = true" />
    <MenuOverlay v-model="isMenuOpen" />
    <slot />
    <AppFooter />
  </div>
</template>

<script setup>
import { ref } from "vue";

const isMenuOpen = ref(false);
</script>
