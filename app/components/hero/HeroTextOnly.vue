<template>
  <section class="hero">
    <div class="container">
      <div class="heading text-center">
        <h1>{{ title }}</h1>
        <p>
          {{ description }}
        </p>
        <div
          v-if="buttonOne || buttonTwo"
          class="flex max-lg:flex-col gap-4 justify-center items-center"
        >
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
    </div>
  </section>
</template>

<script setup>
const props = defineProps({
  title: String,
  description: String,
  buttonOne: Object,
  buttonTwo: Object,
});
</script>

<style lang="scss" scoped></style>
