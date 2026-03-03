<template>
  <section class="bg-dark-primary overflow-hidden">
    <img src="~/assets/img/bg-shape.webp" class="absolute bottom-0 -right-24" />
    <div class="container">
      <div class="heading text-center">
        <h2>Trusted By</h2>
        <p>Organizations modernizing banking and payments with Arkam.</p>
      </div>
      <div class="mt-16">
        <ClientOnly>
          <swiper
            :modules="[Autoplay]"
            :slides-per-view="1"
            :space-between="50"
            :autoplay="{
              delay: 2500,
              disableOnInteraction: false,
              pauseOnMouseEnter: true,
            }"
            :breakpoints="{
              1024: {
                slidesPerView: 2,
              },
              1280: {
                slidesPerView: 3,
              },
            }"
          >
            <swiper-slide v-for="item in items" class="h-auto!">
              <div
                class="bg-white p-8 rounded-2xl flex flex-col justify-between lg:min-h-[430px] h-full"
              >
                <div class="space-y-6">
                  <svg
                    width="46"
                    height="42"
                    viewBox="0 0 46 42"
                    fill="none"
                    xmlns="http://www.w3.org/2000/svg"
                  >
                    <path
                      d="M14.3142 0C4.56835 9.45173 0 19.5133 0 28.5076C0 35.8251 5.48202 41.1608 10.964 41.1608C15.8369 41.1608 19.7962 37.1972 19.7962 32.3188C19.7962 26.0685 15.2278 22.8671 8.52759 22.8671C8.52759 15.3972 10.8118 10.9762 17.9688 3.65873L14.3142 0ZM39.7446 0C29.9988 9.45173 25.4305 19.5133 25.4305 28.5076C25.4305 35.8251 30.9125 41.1608 36.3945 41.1608C41.2674 41.1608 45.2267 37.1972 45.2267 32.3188C45.2267 26.0685 40.6583 22.8671 33.9581 22.8671C33.9581 15.3972 36.2422 10.9762 43.3993 3.65873L39.7446 0Z"
                      fill="#0B1F2A"
                    />
                  </svg>
                  <p>{{ item.description }}</p>
                </div>

                <div
                  class="flex max-lg:flex-col lg:items-center max-lg:gap-3 lg:gap-6 mt-6"
                >
                  <div
                    class="w-[63px] h-[63px] bg-[#E1EDFB] rounded-full"
                  ></div>
                  <div>
                    <p class="font-bold">{{ item.name }}</p>
                    <p>{{ item.position }}</p>
                  </div>
                </div>
              </div>
            </swiper-slide>
          </swiper>
        </ClientOnly>
      </div>
    </div>
  </section>
</template>

<script setup>
import { Swiper, SwiperSlide } from "swiper/vue";
import { Autoplay } from "swiper/modules";
import "swiper/css";

const items = [
  {
    name: "John Carter",
    position: "CEO at Webflow Agency",
    description:
      "Arkam let us launch a new digital proposition alongside our existing core, without a risky big-bang migration. We now deliver new products in weeks instead of quarters.”",
    pic: "",
  },
  {
    name: "John Carter",
    position: "CEO at Webflow Agency",
    description:
      "Arkam let us launch a new digital proposition alongside our existing core, without a risky big-bang migration. We now deliver new products in weeks instead of quarters.”",
    pic: "",
  },
  {
    name: "John Carter",
    position: "CEO at Webflow Agency",
    description:
      "Arkam let us launch a new digital proposition alongside our existing core, without a risky big-bang migration. We now deliver new products in weeks instead of quarters.”",
    pic: "",
  },
  {
    name: "John Carter",
    position: "CEO at Webflow Agency",
    description:
      "Arkam let us launch a new digital proposition alongside our existing core, without a risky big-bang migration. We now deliver new products in weeks instead of quarters.”",
    pic: "",
  },
  {
    name: "John Carter",
    position: "CEO at Webflow Agency",
    description:
      "Arkam let us launch a new digital proposition alongside our existing core, without a risky big-bang migration. We now deliver new products in weeks instead of quarters.”",
    pic: "",
  },
];
</script>

<style lang="scss" scoped></style>
