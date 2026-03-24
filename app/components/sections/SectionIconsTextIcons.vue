<template>
  <section class="bg-tertiary/60">
    <div class="container">
      <div
        class="bg-dark-bg overflow-hidden max-lg:px-6 rounded-3xl w-full lg:min-h-[55vh] flex max-lg:flex-col items-center justify-between max-lg:gap-6 relative"
      >
        <div
          class="absolute -top-32 -left-32 h-80 w-80 rounded-full bg-radial-[at_center] from-[#8FFDFD]/25 via-[#00A6A6]/12 to-transparent blur-3xl lg:h-[32rem] lg:w-[32rem] lg:blur-[140px]"
        ></div>
        <div
          class="absolute lg:-top-32 max-lg:bottom-0 -right-32 h-80 w-80 rounded-full bg-radial-[at_center] from-[#8FFDFD]/25 via-[#00A6A6]/12 to-transparent blur-3xl lg:h-[32rem] lg:w-[32rem] lg:blur-[140px]"
        ></div>
        <div class="lg:w-full max-lg:-rotate-90">
          <img src="/images/left-icons.svg" />
        </div>
        <div class="heading text-center">
          <h2 class="text-white!">{{ title }}</h2>
          <p class="text-white!">
            {{ description }}
          </p>
        </div>
        <div class="lg:w-full max-lg:-rotate-90">
          <img src="/images/right-icons.svg" alt="" />
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
const props = defineProps(["title", "description"]);
</script>

<style lang="scss" scoped></style>
