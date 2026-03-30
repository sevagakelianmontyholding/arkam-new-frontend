<template>
  <section>
    <div class="container">
      <div
        class="flex max-lg:flex-col max-lg:gap-8 lg:gap-16 items-center lg:justify-between border-b border-[#103B50]/20"
      >
        <div class="heading w-full">
          <h2>{{ title }}</h2>
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
        <div class="w-full">
          <img :src="image" alt="" />
        </div>
      </div>
    </div>

    <div class="container max-lg:mt-12 lg:mt-16">
      <div
        class="flex max-lg:flex-col max-lg:gap-8 lg:gap-16 lg:justify-between"
      >
        <div class="space-y-6" v-for="(item, index) in items" :key="index">
          <div
            class="w-[72px] h-[72px] rounded-full flex items-center justify-center bg-tertiary"
            v-html="item.icon"
          />
          <h4>{{ item.title }}</h4>
          <p>{{ item.description }}</p>
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
  "items",
]);
</script>

<style lang="scss" scoped></style>
