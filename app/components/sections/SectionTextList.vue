<template>
  <section>
    <div class="container">
      <div class="flex max-lg:flex-col max-lg:gap-16 lg:gap-24 lg:items-center">
        <div class="lg:w-2/5">
          <div class="heading">
            <h2>{{ title }}</h2>
            <p>
              {{ description }}
            </p>
          </div>
        </div>

        <div class="space-y-6 lg:w-3/5">
          <List :items="items" />
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
const props = defineProps(["title", "description", "items"]);
</script>

<style lang="scss" scoped></style>
