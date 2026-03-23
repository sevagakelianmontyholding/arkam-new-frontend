<template>
  <section
    ref="bankingSection"
    class="relative overflow-hidden lg:min-h-screen lg:py-16!"
  >
    <div class="container h-full">
      <div
        class="flex h-full max-lg:flex-col gap-16 lg:justify-between lg:items-center"
      >
        <div class="lg:w-1/2">
          <div class="heading mb-14">
            <h2>Digital Banking Platform</h2>
            <p>
              Ready-made digital experiences for every segment, powered by the
              same composable core.
            </p>
          </div>

          <!-- Desktop -->
          <div class="max-lg:hidden">
            <!-- LEFT COLUMN: text only -->
            <div class="relative min-h-[30vh]">
              <div
                v-for="(item, index) in items"
                :key="`content-${item.id}`"
                class="absolute inset-0"
                :class="{ 'pointer-events-none': activeIndex !== index }"
                :ref="(el) => setContentRef(el, index)"
              >
                <div class="space-y-6">
                  <p>{{ item.number }}</p>

                  <h3 class="text-3xl text-dark-primary">
                    {{ item.title }}
                  </h3>

                  <p>
                    {{ item.description }}
                  </p>

                  <div class="divider mt-8!"></div>
                </div>
              </div>
            </div>
            <div class="lg:mt-10">
              <NuxtLink to="/" class="a-button">
                Explore digital banking use cases
              </NuxtLink>
            </div>
          </div>
        </div>
        <!-- RIGHT COLUMN: images only -->
        <div class="max-lg:hidden relative lg:w-1/2 flex items-center">
          <div
            v-for="(item, index) in items"
            :key="`image-${item.id}`"
            class="absolute inset-0 flex items-center justify-center"
            :class="{ 'pointer-events-none': activeIndex !== index }"
            :ref="(el) => setImageRef(el, index)"
          >
            <div
              class="bg-[#F6F9F8] overflow-hidden rounded-4xl p-12 w-full flex items-center justify-center"
            >
              <img
                :src="item.image"
                :alt="item.title"
                class="max-w-full object-contain"
              />
            </div>
          </div>
        </div>
      </div>

      <!-- Mobile -->
      <div class="lg:hidden mt-10 space-y-6">
        <div
          v-for="(item, index) in items"
          :key="item.id"
          class="space-y-6 py-6"
        >
          <div class="max-lg:space-y-4">
            <p>{{ item.number }}</p>

            <h3 class="text-3xl text-dark-primary max-lg:text-2xl">
              {{ item.title }}
            </h3>

            <p>
              {{ item.description }}
            </p>
          </div>

          <div
            class="bg-[#F6F9F8] rounded-4xl w-full flex items-center justify-center"
          >
            <img
              :src="item.image"
              :alt="item.title"
              class="max-w-full object-contain"
            />
          </div>

          <div class="divider"></div>
        </div>
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

const setContentRef = (el, index) => {
  if (el) contentRefs.value[index] = el;
};

const setImageRef = (el, index) => {
  if (el) imageRefs.value[index] = el;
};

let mm = null;
let ctx = null;
let resizeTimer = null;
let initTimer = null;

function resetRefArrays() {
  contentRefs.value = [];
  imageRefs.value = [];
}

function clearAllInlineStyles() {
  const els = [
    bankingSection.value,
    ...contentRefs.value,
    ...imageRefs.value,
  ].filter(Boolean);

  gsap.set(els, { clearProps: "all" });
}

function killOwnScrollTriggers() {
  const section = bankingSection.value;
  if (!section) return;

  ScrollTrigger.getAll().forEach((st) => {
    const trigger = st.trigger;
    const pin = st.pin;

    if (trigger === section || pin === section) {
      st.kill();
    }
  });
}

function cleanup() {
  clearTimeout(resizeTimer);
  clearTimeout(initTimer);
  window.removeEventListener("resize", handleResize);

  killOwnScrollTriggers();
  ctx?.revert();
  mm?.revert();

  ctx = null;
  mm = null;
}

function initDesktop() {
  const section = bankingSection.value;
  const contents = contentRefs.value.filter(Boolean);
  const images = imageRefs.value.filter(Boolean);

  if (!section || !contents.length || !images.length) return;

  killOwnScrollTriggers();
  ctx?.revert();

  ctx = gsap.context(() => {
    ScrollTrigger.saveStyles([section, ...contents, ...images]);

    activeIndex.value = 0;

    gsap.set(section, {
      backgroundColor: items.value[0].bg,
    });

    contents.forEach((el, i) => {
      gsap.set(el, {
        autoAlpha: i === 0 ? 1 : 0,
        zIndex: items.value.length - i,
        y: i === 0 ? 0 : 30,
      });
    });

    images.forEach((el, i) => {
      gsap.set(el, {
        autoAlpha: i === 0 ? 1 : 0,
        zIndex: items.value.length - i,
        y: i === 0 ? 0 : 30,
        scale: i === 0 ? 1 : 0.96,
      });
    });

    const totalSegments = items.value.length - 1;

    const tl = gsap.timeline({
      defaults: { ease: "none" },
      scrollTrigger: {
        trigger: section,
        start: "top top",
        end: () => `+=${window.innerHeight * totalSegments}`,
        scrub: 1,
        pin: true,
        anticipatePin: 1,
        invalidateOnRefresh: true,
        refreshPriority: 1,
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

      const start = i - 1;

      tl.to(
        section,
        {
          backgroundColor: items.value[i].bg,
          duration: 0.35,
        },
        start,
      );

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
  }, bankingSection.value);

  ScrollTrigger.refresh();
}

function handleResize() {
  clearTimeout(resizeTimer);
  resizeTimer = setTimeout(() => {
    ScrollTrigger.refresh();
  }, 150);
}

onMounted(async () => {
  await nextTick();

  resetRefArrays();

  initTimer = setTimeout(() => {
    requestAnimationFrame(() => {
      requestAnimationFrame(() => {
        mm = gsap.matchMedia();

        mm.add("(min-width: 1024px)", () => {
          initDesktop();
          window.addEventListener("resize", handleResize);

          return () => {
            window.removeEventListener("resize", handleResize);
            killOwnScrollTriggers();
            ctx?.revert();
          };
        });

        mm.add("(max-width: 1023px)", () => {
          activeIndex.value = 0;
          killOwnScrollTriggers();
          clearAllInlineStyles();

          return () => {
            clearAllInlineStyles();
          };
        });

        ScrollTrigger.refresh();
      });
    });
  }, 0);
});

onUnmounted(() => {
  cleanup();
});
</script>
