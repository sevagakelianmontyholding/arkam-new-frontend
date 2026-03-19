<template>
  <section
    ref="bankingSection"
    class="relative overflow-hidden lg:min-h-screen"
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
import { ref, onMounted, onUnmounted, nextTick } from "vue";
import { gsap } from "gsap";
import { ScrollTrigger } from "gsap/ScrollTrigger";

gsap.registerPlugin(ScrollTrigger);

const bankingSection = ref(null);
const slideRefs = ref([]);
const contentRefs = ref([]);
const imageRefs = ref([]);

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

const setSlideRef = (el, index) => {
  if (el) slideRefs.value[index] = el;
};

const setContentRef = (el, index) => {
  if (el) contentRefs.value[index] = el;
};

const setImageRef = (el, index) => {
  if (el) imageRefs.value[index] = el;
};

let mm;
let ctx;
let resizeTimer;

function clearAllInlineStyles() {
  gsap.set(
    [
      bankingSection.value,
      ...slideRefs.value,
      ...contentRefs.value,
      ...imageRefs.value,
    ],
    { clearProps: "all" },
  );
}

function initDesktop() {
  ctx?.revert();

  ctx = gsap.context(() => {
    const section = bankingSection.value;
    const slides = slideRefs.value;
    const contents = contentRefs.value;
    const images = imageRefs.value;

    if (!section || !slides.length) return;

    // Save original styles so matchMedia cleanup can restore properly
    ScrollTrigger.saveStyles([section, ...slides, ...contents, ...images]);

    activeIndex.value = 0;

    gsap.set(section, {
      backgroundColor: items.value[0].bg,
    });

    slides.forEach((slide, i) => {
      gsap.set(slide, {
        autoAlpha: i === 0 ? 1 : 0,
        zIndex: items.value.length - i,
      });
    });

    contents.forEach((el, i) => {
      gsap.set(el, {
        autoAlpha: i === 0 ? 1 : 0,
        y: i === 0 ? 0 : 30,
      });
    });

    images.forEach((el, i) => {
      gsap.set(el, {
        autoAlpha: i === 0 ? 1 : 0,
        y: i === 0 ? 0 : 30,
        scale: i === 0 ? 1 : 0.96,
      });
    });

    const segment = 1; // one timeline unit per panel
    const totalSegments = items.value.length - 1;

    const tl = gsap.timeline({
      defaults: { ease: "none" },
      scrollTrigger: {
        trigger: section,
        start: "top top",
        end: () => `+=${window.innerHeight * totalSegments}`,
        scrub: 1,
        pin: true,
        invalidateOnRefresh: true,
        onRefresh: () => {
          // Keep progress and measurements fresh after resize
        },
        onUpdate: (self) => {
          const raw = self.progress * totalSegments;
          const index = Math.min(
            items.value.length - 1,
            Math.max(0, Math.round(raw)),
          );
          activeIndex.value = index;
        },
      },
    });

    for (let i = 1; i < items.value.length; i++) {
      const prevContent = contents[i - 1];
      const nextContent = contents[i];
      const prevImage = images[i - 1];
      const nextImage = images[i];
      const prevSlide = slides[i - 1];
      const nextSlide = slides[i];

      const start = (i - 1) * segment;

      // background transition
      tl.to(
        section,
        {
          backgroundColor: items.value[i].bg,
          duration: 0.35,
        },
        start,
      );

      // outgoing
      tl.to(
        prevContent,
        {
          autoAlpha: 0,
          y: -24,
          duration: 0.25,
        },
        start,
      );

      tl.to(
        prevImage,
        {
          autoAlpha: 0,
          y: -24,
          scale: 0.96,
          duration: 0.25,
        },
        start,
      );

      // hide previous / show next slightly later
      tl.to(
        prevSlide,
        {
          autoAlpha: 0,
          duration: 0.01,
        },
        start + 0.24,
      );

      tl.to(
        nextSlide,
        {
          autoAlpha: 1,
          duration: 0.01,
        },
        start + 0.24,
      );

      // incoming
      tl.fromTo(
        nextContent,
        {
          autoAlpha: 0,
          y: 24,
        },
        {
          autoAlpha: 1,
          y: 0,
          duration: 0.28,
        },
        start + 0.24,
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
          duration: 0.3,
        },
        start + 0.24,
      );
    }

    ScrollTrigger.refresh();
  }, bankingSection.value);
}

function handleResize() {
  clearTimeout(resizeTimer);
  resizeTimer = setTimeout(() => {
    ScrollTrigger.refresh();
  }, 150);
}

onMounted(async () => {
  await nextTick();

  mm = gsap.matchMedia();

  mm.add("(min-width: 1024px)", () => {
    initDesktop();
    window.addEventListener("resize", handleResize);

    return () => {
      window.removeEventListener("resize", handleResize);
      ctx?.revert();
    };
  });

  mm.add("(max-width: 1023px)", () => {
    activeIndex.value = 0;
    clearAllInlineStyles();

    return () => {
      clearAllInlineStyles();
    };
  });
});

onUnmounted(() => {
  clearTimeout(resizeTimer);
  window.removeEventListener("resize", handleResize);
  ctx?.revert();
  mm?.revert();
});
</script>
