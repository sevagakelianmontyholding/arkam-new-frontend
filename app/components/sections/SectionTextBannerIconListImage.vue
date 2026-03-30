<template>
  <section>
    <div class="container">
      <div class="heading lg:max-w-[60%]">
        <h2>{{ title }}</h2>
        <p>{{ description }}</p>
      </div>
      <div
        class="grid grid-cols-2 max-lg:grid-cols-1 lg:gap-16 max-lg:gap-6 rounded-3xl lg:mt-10 max-lg:mt-6 bg-tertiary overflow-hidden relative"
      >
        <img
          src="/images/liveness-detection-bg.webp"
          class="absolute z-0 w-full h-full top-0 left-0 object-cover"
          alt=""
        />
        <div
          class="bg-[#C1DEDB]/30 flex flex-col justify-center lg:rounded-tr-[80px] relative z-10 lg:rounded-br-[80px] max-lg:p-6 lg:p-15"
        >
          <IconList :items="items" :white-icons="true" />
        </div>
        <div class="flex flex-col lg:py-10 relative z-10 justify-center">
          <img class="lg:w-[80%]" :src="image" alt="" />
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
import IconList from "../IconList.vue";

const props = defineProps(["title", "description", "items", "image"]);
</script>

<style lang="scss" scoped></style>
