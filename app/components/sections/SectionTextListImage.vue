<template>
  <section>
    <div class="container">
      <div
        class="flex max-lg:flex-col lg:items-center lg:gap-24 max-lg:gap-8 lg:justify-between"
      >
        <div class="heading w-full">
          <h2 v-if="title">{{ title }}</h2>
          <p v-if="description">{{ description }}</p>
          <List :items="items" />
        </div>
        <div
          class="w-full rounded-4xl overflow-hidden"
          :class="[
            darkImage ? 'bg-dark-bg' : 'bg-tertiary',
            noImagePadding
              ? 'py-0 px-0'
              : 'py-10 px-6 flex justify-center items-center',
          ]"
        >
          <div>
            <img :src="image" alt="" />
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
const props = defineProps([
  "title",
  "description",
  "image",
  "items",
  "darkImage",
  "noImagePadding",
]);
</script>

<style lang="scss" scoped></style>
