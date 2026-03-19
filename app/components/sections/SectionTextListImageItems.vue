<template>
  <section :class="dark && 'bg-dark-bg'">
    <div class="container flex flex-col lg:gap-24 max-lg:gap-16">
      <div
        v-for="(item, index) in items"
        :key="index"
        class="flex max-lg:flex-col-reverse max-lg:gap-6 lg:gap-24 lg:justify-between lg:items-center"
        :class="index % 2 != 0 && 'lg:flex-row-reverse'"
      >
        <div class="heading w-full">
          <h2>{{ item.title }}</h2>
          <p v-html="item.description" />
          <List :dark="dark" :items="item.items" :itemsGrid="item.itemsGrid" />
        </div>
        <div class="w-full">
          <img class="rounded-2xl w-full" :src="item.image" alt="" />
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
const props = defineProps(["items", "dark"]);
</script>

<style lang="scss" scoped></style>
