<template>
  <section class="bg-dark-bg">
    <div class="container">
      <div
        class="flex max-lg:flex-col max-lg:gap-16 lg:gap-16 xl:gap-30 2xl:gap-50 lg:justify-between lg:items-center"
      >
        <div class="heading lg:w-1/3">
          <h2>{{ title }}</h2>
          <p>{{ description }}</p>
        </div>
        <div
          class="lg:w-3/5 bg-tertiary max-lg:rounded-2xl rounded-2xl max-lg:p-3 lg:p-6"
        >
          <img class="w-full" :src="image" />
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
const props = defineProps(["title", "description", "image"]);
</script>

<style lang="scss" scoped></style>
