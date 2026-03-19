<template>
  <section class="bg-[#00A6A6]/3">
    <div class="container">
      <div
        class="flex max-lg:flex-col lg:gap-16 max-lg:gap-6 lg:items-center lg:justify-between"
      >
        <div class="w-full heading">
          <h2>{{ title }}</h2>
          <p>{{ description }}</p>
          <div class="flex max-lg:flex-col gap-6" v-if="buttonOne || buttonTwo">
            <NuxtLink
              class="a-button secondary"
              :to="buttonOne.link"
              v-if="buttonOne"
              >{{ buttonOne.text }}</NuxtLink
            >
            <NuxtLink
              class="a-button tertiary"
              :to="buttonTwo.link"
              v-if="buttonTwo"
              >{{ buttonTwo.text }}</NuxtLink
            >
          </div>
        </div>
        <div class="w-full flex items-center justify-center">
          <img :class="imageMaxWidth && 'max-w-[450px]'" :src="image" />
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
const props = defineProps([
  "title",
  "description",
  "buttonOne",
  "buttonTwo",
  "image",
  "imageMaxWidth",
]);
</script>

<style lang="scss" scoped></style>
