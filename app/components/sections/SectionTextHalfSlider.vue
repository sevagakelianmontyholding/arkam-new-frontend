<template>
  <section class="bg-gray">
    <div class="container">
      <div class="heading lg:max-w-[60%]">
        <h2>{{ title }}</h2>
        <p>{{ description }}</p>
      </div>
    </div>

    <div class="container-left">
      <div
        class="flex max-lg:flex-col-reverse max-lg:gap-8 lg:gap-16 lg:justify-between max-lg:mt-4 lg:mt-16"
      >
        <div class="lg:w-1/3 flex max-lg:justify-center gap-3">
          <div
            class="lg:w-[72px] lg:h-[72px] max-lg:w-[50px] max-lg:h-[50px] rounded-full flex items-center justify-center cursor-pointer hover:opacity-80"
            @click="prevSlide"
            :class="isBeginning ? 'bg-[#B1B2B2]/50' : 'bg-secondary'"
          >
            <svg
              width="21"
              height="21"
              viewBox="0 0 21 21"
              fill="none"
              xmlns="http://www.w3.org/2000/svg"
            >
              <path
                d="M19.667 10.3333H1.00033M1.00033 10.3333L10.3337 1M1.00033 10.3333L10.3337 19.6667"
                stroke="#103B50"
                stroke-width="2"
                stroke-linecap="round"
                stroke-linejoin="round"
              />
            </svg>
          </div>
          <div
            class="lg:w-[72px] lg:h-[72px] max-lg:w-[50px] max-lg:h-[50px] rounded-full flex items-center justify-center cursor-pointer hover:opacity-80"
            @click="nextSlide"
            :class="isEnd ? 'bg-[#B1B2B2]/50' : 'bg-secondary'"
          >
            <svg
              width="21"
              height="21"
              viewBox="0 0 21 21"
              fill="none"
              xmlns="http://www.w3.org/2000/svg"
            >
              <path
                d="M1 10.3333H19.6667M19.6667 10.3333L10.3333 1M19.6667 10.3333L10.3333 19.6667"
                stroke="#103B50"
                stroke-width="2"
                stroke-linecap="round"
                stroke-linejoin="round"
              />
            </svg>
          </div>
        </div>
        <div class="lg:w-2/3">
          <ClientOnly>
            <swiper
              @swiper="onSwiper"
              @slideChange="setSwiperState"
              :modules="[Autoplay]"
              :slides-per-view="1"
              :space-between="16"
              :breakpoints="{
                1024: {
                  slidesPerView: 1.75,
                },
                1280: {
                  slidesPerView: 2.25,
                },
              }"
            >
              <swiper-slide
                v-for="(item, index) in sliderItems"
                class="h-auto!"
              >
                <div
                  class="bg-white p-8 rounded-2xl flex flex-col justify-between h-full"
                >
                  <div class="space-y-6">
                    <div
                      class="bg-tertiary w-[60px] h-[60px] rounded-full flex items-center justify-center font-albra-book font-bold text-2xl"
                    >
                      {{ index + 1 }}
                    </div>
                    <h4>{{ item.title }}</h4>
                    <p>{{ item.description }}</p>
                  </div>
                </div>
              </swiper-slide>
            </swiper>
          </ClientOnly>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
const props = defineProps(["title", "description", "sliderItems"]);
import { Swiper, SwiperSlide } from "swiper/vue";
import { Autoplay } from "swiper/modules";
import "swiper/css";

const swiperInstance = ref(null);
const isBeginning = ref(true);
const isEnd = ref(false);

const setSwiperState = (swiper) => {
  swiperInstance.value = swiper;
  isBeginning.value = swiper.isBeginning;
  isEnd.value = swiper.isEnd;
};

const nextSlide = () => {
  if (!isEnd.value) swiperInstance.value?.slideNext();
};

const prevSlide = () => {
  if (!isBeginning.value) swiperInstance.value?.slidePrev();
};

const onSwiper = (s) => {
  swiperInstance.value = s;
};
</script>

<style lang="scss" scoped></style>
