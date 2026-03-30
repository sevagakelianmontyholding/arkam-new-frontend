<template>
  <section class="bg-gray">
    <div class="container">
      <div class="heading lg:max-w-[60%]">
        <h2>{{ title }}</h2>
        <p>{{ description }}</p>
      </div>
    </div>
  </section>
</template>

<script setup>
const props = defineProps(["title", "description", "sliderItems"]);
</script>

<style lang="scss" scoped></style>
