<template>
  <div
    v-if="modelValue"
    class="fixed inset-0 z-50 bg-[#021826] text-white overflow-y-auto"
  >
    <!-- glow -->
    <div
      class="pointer-events-none absolute inset-0 bg-[radial-gradient(circle_at_center,_rgba(0,166,166,0.18),_transparent_45%)]"
    ></div>

    <div class="relative container min-h-screen py-8 lg:py-10">
      <!-- top -->
      <div class="flex items-center justify-between mb-10 lg:mb-16">
        <Logo :dark="true" />

        <button
          type="button"
          aria-label="Close menu"
          class="w-10 h-10 flex items-center justify-center"
          @click="emit('update:modelValue', false)"
        >
          <svg
            width="18"
            height="18"
            viewBox="0 0 18 18"
            fill="none"
            xmlns="http://www.w3.org/2000/svg"
          >
            <line
              x1="1"
              y1="1"
              x2="17"
              y2="17"
              stroke="white"
              stroke-width="1.5"
              stroke-linecap="round"
            />
            <line
              x1="17"
              y1="1"
              x2="1"
              y2="17"
              stroke="white"
              stroke-width="1.5"
              stroke-linecap="round"
            />
          </svg>
        </button>
      </div>

      <!-- DESKTOP -->
      <div
        class="hidden lg:grid lg:grid-cols-[1.1fr_0.9fr] gap-16 min-h-[70vh]"
      >
        <!-- left big items -->
        <div class="flex flex-col justify-center">
          <button
            v-for="(item, index) in menuItems"
            :key="item.label"
            type="button"
            class="flex items-start gap-5 text-left transition-opacity duration-300 py-4"
            :class="
              activeIndex === index
                ? 'opacity-100'
                : 'opacity-35 hover:opacity-80'
            "
            @mouseenter="activeIndex = index"
            @click="activeIndex = index"
          >
            <span class="text-sm pt-3 min-w-[28px]">
              {{ String(index + 1).padStart(2, "0") }}
            </span>

            <span class="font-albra text-[56px] leading-[0.95]">
              {{ item.label }}
            </span>
          </button>
        </div>

        <!-- right submenus -->
        <div class="flex items-center">
          <div
            v-if="activeItem?.groups?.length"
            class="w-full h-full flex flex-col justify-between max-w-[430px] ml-auto py-6"
          >
            <div
              v-for="group in activeItem.groups"
              :key="group.title"
              class="flex flex-col"
            >
              <h3 class="text-[28px] leading-none font-medium mb-5">
                {{ group.title }}
              </h3>

              <ul class="space-y-3">
                <li v-for="link in group.links" :key="link.label">
                  <NuxtLink
                    :to="link.to"
                    class="text-white/75 hover:text-[#00A6A6] transition-colors text-base"
                    @click="emit('update:modelValue', false)"
                  >
                    {{ link.label }}
                  </NuxtLink>
                </li>
              </ul>
            </div>
          </div>
        </div>
      </div>

      <!-- MOBILE -->
      <div class="lg:hidden">
        <div class="divide-y divide-white/10 border-y border-white/10">
          <div
            v-for="(item, index) in menuItems"
            :key="item.label"
            class="py-5"
          >
            <button
              type="button"
              class="w-full flex items-start justify-between gap-4 text-left"
              @click="toggleAccordion(index)"
            >
              <div class="flex items-start gap-4">
                <span class="text-xs pt-2 min-w-[22px] text-white/70">
                  {{ String(index + 1).padStart(2, "0") }}
                </span>

                <span class="font-albra text-[34px] leading-none">
                  {{ item.label }}
                </span>
              </div>

              <span class="text-white/80 text-2xl leading-none mt-1">
                {{ openAccordion === index ? "−" : "+" }}
              </span>
            </button>

            <transition name="accordion">
              <div v-if="openAccordion === index" class="pl-[38px] pt-5">
                <div
                  v-for="group in item.groups"
                  :key="group.title"
                  class="mb-8 last:mb-0"
                >
                  <h3 class="text-xl mb-4 font-medium">
                    {{ group.title }}
                  </h3>

                  <ul class="space-y-3">
                    <li v-for="link in group.links" :key="link.label">
                      <NuxtLink
                        :to="link.to"
                        class="block text-white/75 hover:text-[#00A6A6] transition-colors text-sm"
                        @click="emit('update:modelValue', false)"
                      >
                        {{ link.label }}
                      </NuxtLink>
                    </li>
                  </ul>
                </div>
              </div>
            </transition>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script setup>
import { computed, ref, watch, onBeforeUnmount } from "vue";
import Logo from "./Logo.vue";

const props = defineProps({
  modelValue: {
    type: Boolean,
    default: false,
  },
});

const emit = defineEmits(["update:modelValue"]);

const menuItems = [
  {
    label: "Products",
    groups: [
      {
        title: "Digital Core Banking",
        links: [
          {
            label: "Interest-Based Accounts",
            to: "/products/digital-core-banking/accounts/interest-based-accounts",
          },
          {
            label: "Multi-Currency Accounts",
            to: "/products/digital-core-banking/accounts/multi-currency-accounts",
          },
          {
            label: "Financial Accounting & Reporting",
            to: "/products/digital-core-banking/financial-accounting-and-reporting",
          },
          {
            label: "Security & Compliance",
            to: "/products/digital-core-banking/security-and-compliance",
          },
          {
            label: "Currency Exchange",
            to: "/products/digital-core-banking/currency-exchange",
          },
          {
            label: "Tariffs & Fees",
            to: "/products/digital-core-banking/tariffs-and-fees",
          },
        ],
      },
      {
        title: "Digital Banking Platform",
        links: [
          {
            label: "One Platform, Multiple Channels",
            to: "/products/digital-banking-platform/one-platform-multiple-channels",
          },
          {
            label: "Mobile Banking (Android and iOS)",
            to: "/products/digital-banking-platform/mobile-banking",
          },
          {
            label: "Web and Corporate Banking Portals",
            to: "/products/digital-banking-platform/web-and-corporate-banking-portals",
          },
          {
            label: "Agent Banking",
            to: "/products/digital-banking-platform/agent-banking",
          },
          {
            label: "ATM Network Integrations",
            to: "/products/digital-banking-platform/atm-network-integrations",
          },
          {
            label: "POS and QR Acceptance",
            to: "/products/digital-banking-platform/pos-and-qr-acceptance",
          },
          {
            label: "Branch Teller (Client Cash Desk)",
            to: "/products/digital-banking-platform/branch-teller",
          },
        ],
      },
    ],
  },
  {
    label: "Solutions",
    groups: [
      {
        title: "Solutions",
        // links: [
        //   { label: "Retail Banking", to: "/solutions/retail-banking" },
        //   { label: "Islamic Banking", to: "/solutions/islamic-banking" },
        //   { label: "Microfinance", to: "/solutions/microfinance" },
        // ],
      },
    ],
  },
  {
    label: "Who We Serve",
    groups: [
      {
        title: "Retail Bank",
        links: [
          {
            label: "Digital Onboarding",
            to: "/who-we-serve/retail-bank/digital-onboarding",
          },
        ],
      },
      {
        title: "Neo‑Banks & Fintechs",
        links: [
          {
            label: "Wallet-Led Digital Onboarding",
            to: "/who-we-serve/neo-banks-and-fintechs/wallet-led-digital-onboarding",
          },
        ],
      },
    ],
  },
  {
    label: "Resources",
    groups: [
      {
        title: "Resources",
        // links: [
        //   { label: "Blog", to: "/resources/blog" },
        //   { label: "Case Studies", to: "/resources/case-studies" },
        //   { label: "Downloads", to: "/resources/downloads" },
        // ],
      },
    ],
  },
  {
    label: "Company",
    groups: [
      {
        title: "Company",
        // links: [
        //   { label: "About Us", to: "/company/about" },
        //   { label: "Careers", to: "/company/careers" },
        //   { label: "Contact", to: "/company/contact" },
        // ],
      },
    ],
  },
];

const activeIndex = ref(0);
const openAccordion = ref(0);

const activeItem = computed(() => menuItems[activeIndex.value]);

const toggleAccordion = (index) => {
  openAccordion.value = openAccordion.value === index ? null : index;
};

const handleKeydown = (e) => {
  if (e.key === "Escape") {
    emit("update:modelValue", false);
  }
};

watch(
  () => props.modelValue,
  (isOpen) => {
    if (import.meta.client) {
      document.body.style.overflow = isOpen ? "hidden" : "";
    }

    if (isOpen) {
      activeIndex.value = 0;
      openAccordion.value = 0;

      // ✅ attach ESC listener
      if (import.meta.client) {
        window.addEventListener("keydown", handleKeydown);
      }
    } else {
      // ✅ remove listener when closed
      if (import.meta.client) {
        window.removeEventListener("keydown", handleKeydown);
      }
    }
  },
  { immediate: true },
);

onBeforeUnmount(() => {
  if (import.meta.client) {
    document.body.style.overflow = "";
    window.removeEventListener("keydown", handleKeydown);
  }
});

onBeforeUnmount(() => {
  document.body.style.overflow = "";
});
</script>

<style scoped>
.accordion-enter-active,
.accordion-leave-active {
  transition: all 0.25s ease;
  overflow: hidden;
}

.accordion-enter-from,
.accordion-leave-to {
  opacity: 0;
  max-height: 0;
}

.accordion-enter-to,
.accordion-leave-from {
  opacity: 1;
  max-height: 800px;
}
</style>
