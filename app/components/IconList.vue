<template>
  <div class="flex flex-col max-lg:gap-4 lg:gap-6">
    <div v-for="(item, index) in items" :key="index">
      <div class="flex max-lg:flex-col gap-4">
        <div
          class="w-[60px] h-[60px] rounded-full flex items-center justify-center shrink-0"
          :class="whiteIcons ? 'bg-white' : 'bg-tertiary'"
          v-html="item.icon"
        />
        <div class="space-y-2">
          <h4>{{ item.title }}</h4>
          <p>{{ item.description }}</p>
        </div>
      </div>
      <div class="divider" v-if="index + 1 != items.length"></div>
    </div>
  </div>
</template>

<script setup>
const props = defineProps(["items", "whiteIcons"]);
</script>

<style lang="scss" scoped></style>
