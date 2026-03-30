<template>
  <section>
    <div class="container">
      <div
        class="flex max-lg:flex-col-reverse lg:gap-16 max-lg:gap-8 lg:justify-between items-center"
      >
        <div class="lg:w-[45%]">
          <img class="w-full" :src="image" alt="" />
        </div>
        <div class="lg:w-[55%]">
          <div class="heading">
            <h2>{{ title }}</h2>
            <p>{{ description }}</p>
            <IconList class="mt-10" :items="items" />
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
import IconList from "../IconList.vue";

const props = defineProps(["image", "title", "description", "items"]);
</script>

<style lang="scss" scoped></style>
