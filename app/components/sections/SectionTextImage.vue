<template>
  <section>
    <div class="container">
      <div class="flex max-lg:flex-col lg:gap-24 lg:justify-between">
        <div class="heading w-full">
          <h2>{{ title }}</h2>
          <p>{{ description }}</p>
          <div class="space-y-2" v-for="(item, index) in items" :key="index">
            <h4>{{ item.title }}</h4>
            <p>{{ item.description }}</p>
            <div class="divider" v-if="index + 1 < items.length"></div>
          </div>
        </div>
        <div class="w-full rounded-2xl p-6 bg-tertiary">
          <img :src="image" alt="" />
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
const props = defineProps(["title", "description", "image", "items"]);
</script>

<style lang="scss" scoped></style>
