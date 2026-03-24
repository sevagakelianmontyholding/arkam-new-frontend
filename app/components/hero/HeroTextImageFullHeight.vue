<template>
  <section class="py-0!">
    <div
      class="container flex max-lg:flex-col gap-16 lg:justify-between max-lg:items-center"
    >
      <div class="heading w-full self-center">
        <h1>{{ title }}</h1>
        <p>{{ description }}</p>
        <div v-if="buttonOne || buttonTwo" class="flex max-lg:flex-col gap-4">
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
      <div class="w-full flex lg:justify-end">
        <img :src="image" class="lg:h-screen max-lg:w-full object-contain" />
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
]);
</script>

<style lang="scss" scoped></style>
