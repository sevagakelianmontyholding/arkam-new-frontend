<template>
  <section>
    <div class="container">
      <div
        class="flex max-lg:flex-col max-lg:gap-12 lg:gap-24 lg:justify-between lg:items-center"
      >
        <div class="lg:w-2/5">
          <div class="heading">
            <h2>{{ title }}</h2>
            <p>
              {{ description }}
            </p>
          </div>
        </div>

        <div class="max-lg:space-y-8 lg:space-y-6">
          <div v-for="(item, index) in items" :key="index">
            <div
              class="flex max-lg:flex-col max-lg:gap-2 lg:gap-6 lg:items-center"
            >
              <svg
                width="80"
                height="80"
                viewBox="0 0 80 80"
                fill="none"
                xmlns="http://www.w3.org/2000/svg"
                class="shrink-0"
              >
                <rect
                  width="79.5355"
                  height="79.5355"
                  rx="39.7678"
                  fill="#E2F5F4"
                />
                <path
                  d="M60.3756 37.884V39.7799C60.373 44.2238 58.934 48.5479 56.2732 52.1072C53.6124 55.6665 49.8723 58.2703 45.6107 59.5303C41.3491 60.7904 36.7944 60.6391 32.6259 59.099C28.4573 57.5589 24.8983 54.7126 22.4795 50.9846C20.0608 47.2565 18.9119 42.8465 19.2043 38.4122C19.4967 33.9779 21.2147 29.7569 24.102 26.3787C26.9894 23.0005 30.8913 20.6462 35.226 19.6668C39.5607 18.6875 44.0958 19.1356 48.1551 20.9442M60.3756 23.2817L39.7676 43.9103L33.5852 37.7279"
                  stroke="#00C8C8"
                  stroke-width="3.34183"
                  stroke-linecap="round"
                  stroke-linejoin="round"
                />
              </svg>
              <div>
                <p class="font-semibold">{{ item.title }}</p>
                <p v-if="item.description" class="mt-2">
                  {{ item.description }}
                </p>
              </div>
            </div>

            <div
              class="divider w-20! max-lg:hidden"
              v-if="index + 1 < items.length"
            ></div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
const props = defineProps(["title", "description", "items"]);
</script>

<style lang="scss" scoped></style>
