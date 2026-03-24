<template>
  <div :class="{ 'no-top-padding': noTopPadding }">
    <AppHeader @toggle-menu="isMenuOpen = true" />
    <MenuOverlay v-model="isMenuOpen" />
    <main>
      <slot />
    </main>
    <AppFooter />
  </div>
</template>

<script setup>
import { ref } from "vue";

const isMenuOpen = ref(false);
const route = useRoute();

const noTopPadding = computed(() => {
  return route.meta.noTopPadding === true;
});
</script>
