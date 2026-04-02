<template>
  <section>
    <div class="container">
      <div class="heading">
        <h2>{{ title }}</h2>
        <p>{{ description }}</p>
      </div>
      <div
        class="grid lg:grid-cols-3 max-lg:grid-cols-1 gap-6 max-lg:mt-6 lg:mt-12"
      >
        <div
          v-for="(item, index) in items"
          :key="index"
          class="lg:min-h-[600px] relative rounded-2xl overflow-hidden group p-7 flex items-end"
        >
          <img
            :src="item.image"
            alt=""
            class="absolute w-full h-full object-cover top-0 left-0 z-0"
          />
          <div
            class="w-full h-full z-0 absolute bg-[#000000]/20 top-0 left-0 opacity-100 group-hover:opacity-0 transition-all duration-300"
          ></div>
          <div
            class="w-full h-full absolute z-10 lg:opacity-0 lg:group-hover:opacity-100 transition duration-300 left-0 top-0"
            :class="item.color"
          ></div>

          <div class="relative z-10 space-y-2">
            <h4 class="text-white!">{{ item.title }}</h4>
            <p
              class="text-white! overflow-hidden lg:max-h-0 lg:opacity-0 lg:transition-[max-height,opacity] lg:duration-300 lg:group-hover:max-h-96 lg:group-hover:opacity-100"
            >
              {{ item.description }}
            </p>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
const props = defineProps(["title", "description", "items"]);
</script>

<style lang="css" scoped>
.dark-blue {
  @apply bg-[linear-gradient(360deg,rgba(0,0,0,0.2)_0%,rgba(102,102,102,0.2)_100%),linear-gradient(0deg,rgba(0,0,0,0.2),rgba(0,0,0,0.2)),linear-gradient(0deg,rgba(16,59,80,0.8),rgba(16,59,80,0.8))];
}
.orange {
  @apply bg-[linear-gradient(0deg,rgba(0,0,0,0.2),rgba(0,0,0,0.2)),linear-gradient(0deg,rgba(201,129,81,0.8),rgba(201,129,81,0.8))];
}

.light-blue {
  @apply bg-[linear-gradient(rgba(0,0,0,0.2),rgba(0,0,0,0.2)),linear-gradient(rgba(66,159,154,0.8),rgba(66,159,154,0.8))];
}
</style>
