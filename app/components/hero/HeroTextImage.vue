<template>
  <section class="hero">
    <div
      class="container flex max-lg:flex-col lg:justify-between lg:gap-32 max-lg:gap-6 items-center"
    >
      <div class="heading max-lg:w-full lg:w-[55%]">
        <h1>{{ title }}</h1>
        <p>{{ description }}</p>
        <div v-if="buttonOne || buttonTwo" class="flex max-lg:flex-col gap-6">
          <NuxtLink
            v-if="buttonOne"
            :to="buttonOne.link"
            class="a-button secondary"
            >{{ buttonOne.text }}</NuxtLink
          >
          <NuxtLink
            v-if="buttonTwo"
            :to="buttonTwo.link"
            class="a-button tertiary"
            >{{ buttonTwo.text }}</NuxtLink
          >
        </div>
      </div>
      <div class="max-lg:w-full lg:w-[45%]">
        <img :src="image" />
      </div>
    </div>
  </section>
</template>

<script setup>
const props = defineProps([
  "title",
  "description",
  "image",
  "buttonOne",
  "buttonTwo",
]);
</script>

<style lang="scss" scoped></style>
