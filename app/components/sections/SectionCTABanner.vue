<template>
  <section>
    <div class="container">
      <div
        class="bg-dark-bg min-h-[50vh] p-10 overflow-hidden rounded-2xl relative flex flex-col items-center justify-center"
      >
        <div class="pointer-events-none absolute inset-0 overflow-hidden">
          <div
            class="absolute -top-32 -left-32 h-80 w-80 rounded-full bg-radial-[at_center] from-[#8FFDFD]/25 via-[#00A6A6]/12 to-transparent blur-3xl lg:h-[32rem] lg:w-[32rem] lg:blur-[140px]"
          ></div>

          <div
            class="absolute -bottom-32 -right-32 h-80 w-80 rounded-full bg-radial-[at_center] from-[#8FFDFD]/25 via-[#00A6A6]/12 to-transparent blur-3xl lg:h-[34rem] lg:w-[34rem] lg:blur-[160px]"
          ></div>

          <div
            class="absolute top-1/2 left-1/2 h-64 w-64 -translate-x-1/2 -translate-y-1/2 rounded-full bg-radial-[at_center] from-[#66C3BE]/16 via-[#007D9B]/8 to-transparent blur-3xl lg:h-[24rem] lg:w-[24rem] lg:blur-[120px]"
          ></div>
        </div>
        <div class="heading relative z-10 text-center lg:max-w-[80%]">
          <h2 class="text-white!">{{ title }}</h2>
          <p class="text-white!" v-if="description">{{ description }}</p>
          <div
            v-if="buttonOne || buttonTwo"
            class="flex max-lg:flex-col gap-6 justify-center items-center"
          >
            <NuxtLink
              v-if="buttonOne"
              :to="buttonOne.link"
              class="a-button secondary"
              >{{ buttonOne.text }}</NuxtLink
            >
            <NuxtLink v-if="buttonTwo" :to="buttonTwo.link" class="a-button">{{
              buttonTwo.text
            }}</NuxtLink>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
const props = defineProps(["title", "description", "buttonOne", "buttonTwo"]);
</script>

<style lang="scss" scoped></style>
