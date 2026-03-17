<template>
  <div v-if="items">
    <div>
      <div v-for="(item, index) in items" :key="index">
        <div class="space-y-2">
          <h4 :class="dark && 'text-white!'">{{ item.title }}</h4>
          <p :class="dark && 'text-white!'">{{ item.description }}</p>
        </div>

        <div
          :class="dark && 'dark'"
          class="divider"
          v-if="index + 1 < items?.length"
        ></div>
      </div>
    </div>
  </div>

  <div v-if="itemsGrid">
    <div class="grid grid-cols-2 max-lg:grid-cols-1 gap-6">
      <div
        v-for="(item, index) in itemsGrid"
        :key="index"
        :class="index % 2 == 0 && 'lg:border-r border-[#103B50]/20 pr-3'"
      >
        <div class="space-y-2">
          <h4 :class="dark && 'text-white!'">{{ item.title }}</h4>
          <p :class="dark && 'text-white!'">{{ item.description }}</p>
        </div>

        <div
          :class="dark && 'dark'"
          class="divider lg:hidden"
          v-if="index + 1 < itemsGrid?.length"
        ></div>
      </div>
    </div>
  </div>
</template>

<script setup>
const props = defineProps(["items", "itemsGrid", "dark"]);
</script>

<style lang="scss" scoped></style>
