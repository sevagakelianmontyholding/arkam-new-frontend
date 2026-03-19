<template>
  <section class="bg-dark-bg">
    <div class="container-left">
      <div
        class="flex max-lg:flex-col max-lg:gap-16 lg:gap-16 xl:gap-30 2xl:gap-50 lg:justify-between lg:items-center"
      >
        <div class="heading lg:w-1/3">
          <h2>{{ title }}</h2>
          <p>{{ description }}</p>
        </div>
        <div
          class="lg:w-2/3 bg-tertiary max-lg:rounded-2xl rounded-tl-2xl rounded-bl-2xl p-6 lg:pr-0"
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
