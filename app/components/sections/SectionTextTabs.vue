<template>
  <section class="bg-gray">
    <div class="container">
      <div class="heading text-center">
        <h2>{{ title }}</h2>
        <p>{{ description }}</p>

        <div class="mt-10">
          <ul
            class="bg-tertiary lg:w-max mx-auto rounded-full p-2 flex gap-2 max-lg:overflow-scroll"
          >
            <li
              v-for="(item, index) in tabs"
              :key="index"
              class="text-secondary text-center font-bold rounded-full py-2 px-4 w-fit cursor-pointer whitespace-nowrap lg:min-w-[230px]"
              :class="selectedIndex === index && 'bg-white'"
              @click="
                () => {
                  selectedIndex = index;
                }
              "
            >
              {{ item.title }}
            </li>
          </ul>

          <div class="mt-14">
            <div
              v-for="(item, index) in tabs"
              :class="index === selectedIndex ? 'block' : 'hidden'"
            >
              <img clsss="w-full" :src="item.image" alt="" />
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
const props = defineProps(["title", "description", "tabs"]);
const selectedIndex = ref(0);
</script>

<style lang="scss" scoped></style>
