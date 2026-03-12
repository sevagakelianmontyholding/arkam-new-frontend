<template>
  <section
    ref="bankingSection"
    class="relative overflow-hidden lg:min-h-screen"
    :style="{ backgroundColor: activeItem.bg }"
  >
    <div class="container">
      <div class="heading lg:w-1/2">
        <h2>Digital Banking Platform</h2>
        <p>
          Ready-made digital experiences for every segment, powered by the same
          composable core.
        </p>
      </div>

      <div class="relative lg:min-h-[50vh] mt-10">
        <div
          v-for="(item, index) in items"
          :key="item.id"
          class="banking-slide max-lg:space-y-8 max-lg:py-10 lg:absolute inset-0 lg:grid lg:grid-cols-2 lg:gap-16 lg:items-center"
          :class="{ 'pointer-events-none': activeIndex !== index }"
          :ref="(el) => setSlideRef(el, index)"
        >
          <!-- content -->
          <div class="slide-content" :ref="(el) => setContentRef(el, index)">
            <div class="space-y-6">
              <p>{{ item.number }}</p>

              <h3 class="text-3xl text-dark-primary max-lg:text-2xl">
                {{ item.title }}
              </h3>

              <p>
                {{ item.description }}
              </p>

              <div class="divider mt-16!"></div>
            </div>
          </div>

          <!-- image -->
          <div
            class="slide-image bg-[#F6F9F8] rounded-4xl p-12 w-full h-full flex items-center justify-center"
            :ref="(el) => setImageRef(el, index)"
          >
            <img
              :src="item.image"
              :alt="item.title"
              class="max-w-full object-contain"
            />
          </div>
        </div>
      </div>

      <div class="lg:mt-10">
        <NuxtLink to="/" class="a-button">
          Explore digital banking use cases
        </NuxtLink>
      </div>
    </div>
  </section>
</template>

<script setup>
import { ref, computed, onMounted, onUnmounted } from "vue";
import { gsap } from "gsap";
import { ScrollTrigger } from "gsap/ScrollTrigger";

gsap.registerPlugin(ScrollTrigger);

const mm = gsap.matchMedia();

const bankingSection = ref(null);
const slideRefs = ref([]);
const contentRefs = ref([]);
const imageRefs = ref([]);
let ctx;

const items = ref([
  {
    id: 1,
    number: "01",
    title: "Retail Digital Banking",
    description:
      "Offer mobile and web banking with digital onboarding, accounts, cards, wallets, P2P transfers and bill payment. Personalise journeys with data-driven offers, notifications and limits.",
    image: "/images/db1.webp",
    bg: "#E6EFE9",
  },
  {
    id: 2,
    number: "02",
    title: "SME & Business Banking",
    description:
      "Give SMEs a single workspace for approvals, payroll and bulk payments. Support multi-user access, roles and limits so finance teams can manage company money securely and efficiently.",
    image: "/images/db2.webp",
    bg: "#ECEEEC",
  },
  {
    id: 3,
    number: "03",
    title: "Digital-Only & Neo-Banks",
    description:
      "Launch new digital brands or propositions fast. Use low-code workflows and open APIs to experiment with pricing, bundles and features without disturbing your legacy core.",
    image: "/images/db3.webp",
    bg: "#EEEFE6",
  },
  {
    id: 4,
    number: "04",
    title: "Telco & Super-App Financial Services",
    description:
      "Embed wallets, airtime, eSIM, vouchers and payments into a single super-app. Integrate with existing OSS/BSS systems to add financial services without rebuilding your infrastructure.",
    image: "/images/db2.webp",
    bg: "#E6EBEF",
  },
]);

const activeIndex = ref(0);
const activeItem = computed(() => items.value[activeIndex.value]);

const setSlideRef = (el, index) => {
  if (el) slideRefs.value[index] = el;
};

const setContentRef = (el, index) => {
  if (el) contentRefs.value[index] = el;
};

const setImageRef = (el, index) => {
  if (el) imageRefs.value[index] = el;
};

onMounted(() => {
  mm.add("(min-width: 1024px)", () => {
    ctx = gsap.context(() => {
      const section = bankingSection.value;
      const slides = slideRefs.value;
      const contents = contentRefs.value;
      const images = imageRefs.value;

      slides.forEach((slide, i) => {
        gsap.set(slide, {
          autoAlpha: i === 0 ? 1 : 0,
        });
      });

      contents.forEach((el, i) => {
        gsap.set(el, {
          autoAlpha: i === 0 ? 1 : 0,
          y: i === 0 ? 0 : 24,
        });
      });

      images.forEach((el, i) => {
        gsap.set(el, {
          autoAlpha: i === 0 ? 1 : 0,
          y: i === 0 ? 0 : 24,
          scale: i === 0 ? 1 : 0.96,
        });
      });

      const tl = gsap.timeline({
        scrollTrigger: {
          trigger: section,
          start: "top top",
          end: `+=${items.value.length * 1000}`,
          scrub: 1,
          pin: true,
          anticipatePin: 1,
        },
      });

      items.value.forEach((item, index) => {
        if (index === 0) return;

        const prevSlide = slides[index - 1];
        const nextSlide = slides[index];
        const prevContent = contents[index - 1];
        const nextContent = contents[index];
        const prevImage = images[index - 1];
        const nextImage = images[index];

        tl.addLabel(`step-${index}`);

        tl.to(
          section,
          {
            backgroundColor: item.bg,
            duration: 0.5,
            onStart: () => {
              activeIndex.value = index;
            },
            onReverseComplete: () => {
              activeIndex.value = index - 1;
            },
          },
          `step-${index}`,
        );

        tl.to(
          prevContent,
          {
            autoAlpha: 0,
            y: -24,
            duration: 0.35,
            ease: "power2.out",
          },
          `step-${index}`,
        );

        tl.to(
          prevImage,
          {
            autoAlpha: 0,
            y: -20,
            scale: 0.96,
            duration: 0.4,
            ease: "power2.out",
          },
          `step-${index}`,
        );

        tl.set(prevSlide, { autoAlpha: 0 }, `step-${index}+=0.2`);

        tl.set(nextSlide, { autoAlpha: 1 }, `step-${index}+=0.2`);

        tl.fromTo(
          nextContent,
          {
            autoAlpha: 0,
            y: 24,
          },
          {
            autoAlpha: 1,
            y: 0,
            duration: 0.45,
            ease: "power2.out",
          },
          `step-${index}+=0.2`,
        );

        tl.fromTo(
          nextImage,
          {
            autoAlpha: 0,
            y: 24,
            scale: 1.02,
          },
          {
            autoAlpha: 1,
            y: 0,
            scale: 1,
            duration: 0.5,
            ease: "power2.out",
          },
          `step-${index}+=0.24`,
        );

        tl.to({}, { duration: 0.6 });
      });
    }, bankingSection.value);
  });
});

onUnmounted(() => {
  ctx?.revert();
  mm.revert();
});
</script>
