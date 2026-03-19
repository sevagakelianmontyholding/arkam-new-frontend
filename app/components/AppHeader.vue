<template>
  <header
    :class="[
      'fixed top-0 left-0 w-full z-40 h-(--header-height) transition-all duration-300 ease-out',
      scrolled ? 'bg-white/80 backdrop-blur-md shadow-sm' : 'bg-transparent',
      hiddenHeader ? '-translate-y-full' : 'translate-y-0',
    ]"
  >
    <div class="container h-full flex justify-between items-center">
      <Logo />
      <Hamburger @click="emit('toggle-menu')" />
    </div>
  </header>
</template>

<script setup>
import { ref, onMounted, onBeforeUnmount } from "vue";
import Hamburger from "./Hamburger.vue";

const emit = defineEmits(["toggle-menu"]);

const scrolled = ref(false);
const hiddenHeader = ref(false);
const lastScrollY = ref(0);

const SCROLL_BG_THRESHOLD = 20;
const SCROLL_HIDE_THRESHOLD = 120;

const handleScroll = () => {
  if (!import.meta.client) return;

  const currentScrollY = window.scrollY;

  // white/blur background after slight scroll
  scrolled.value = currentScrollY > SCROLL_BG_THRESHOLD;

  // keep visible near top
  if (currentScrollY <= SCROLL_HIDE_THRESHOLD) {
    hiddenHeader.value = false;
    lastScrollY.value = currentScrollY;
    return;
  }

  // hide on scroll down, show on scroll up
  if (currentScrollY > lastScrollY.value) {
    hiddenHeader.value = true;
  } else {
    hiddenHeader.value = false;
  }

  lastScrollY.value = currentScrollY;
};

onMounted(() => {
  if (!import.meta.client) return;

  lastScrollY.value = window.scrollY;
  window.addEventListener("scroll", handleScroll, { passive: true });
});

onBeforeUnmount(() => {
  if (!import.meta.client) return;
  window.removeEventListener("scroll", handleScroll);
});
</script>
