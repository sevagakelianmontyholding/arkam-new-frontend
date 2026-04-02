<template>
  <HeroTextImage
    title="Wallet-Led Digital Onboarding Built for Speed and Control"
    description="Create a fast onboarding journey that activates a wallet account and unlocks core financial services. Arkam keeps the experience digital-first while supporting controlled steps and auditable outcomes through an API-first design."
    :button-one="{ text: 'Book a Live Demo', link: '/' }"
    :button-two="{ text: 'Contact us', link: '/' }"
    image="/images/wallet-led-digital-onboarding.webp"
  />

  <SectionIconsTextIcons
    title="Platform Foundation"
    description="These journeys are delivered on Arkam’s cloud-native, API-first platform. 
The architecture is modular and microservices-based, designed for rapid iteration and controlled change. Integration is handled through standard APIs and an integration layer so teams can connect to rails, processors and partners without brittle point-to-point builds. Operational visibility is supported through centralised monitoring, logging and tracing practices suitable for regulated environments."
  />

  <SectionTextImagesHoverOverlay
    title="Wallet Account"
    description="Digital Wallet Onboarding & Provisioning"
    :items="walletAccountItems"
  />

  <SectionTextList
    title="FAQ"
    description="Short answers to how Arkam Core fits into your architecture, security model and roadmap."
    :items="faq"
  />

  <SectionCTABanner
    title="Launch and Scale Digital-First Journeys with Arkam"
    description="See how Arkam supports wallet-led onboarding, modern payments, embedded services and digital credit—delivered through a composable platform with integration-first delivery and audit-ready controls."
    :button-one="{ text: 'Book a Live Demo', link: '/' }"
    :button-two="{ text: 'Contact us', link: '/' }"
  />
</template>

<script setup>
import HeroTextImage from "../../../components/hero/HeroTextImage.vue";
import SectionCTABanner from "../../../components/sections/SectionCTABanner.vue";
import SectionIconsTextIcons from "../../../components/sections/SectionIconsTextIcons.vue";
import SectionTextImagesHoverOverlay from "../../../components/sections/SectionTextImagesHoverOverlay.vue";
import SectionTextList from "../../../components/sections/SectionTextList.vue";

const faq = [
  {
    title:
      "Can we launch a wallet proposition fast without locking into a single provider stack?",
    description:
      "Yes. Arkam is integration-first. Wallet, payments, card and value-added services can connect to approved partners through APIs, so you can evolve providers without rebuilding the channel layer.",
  },
  {
    title:
      "Do we need a full core replacement to launch digital-first journeys?",
    description:
      "No. A common approach is to deploy Arkam alongside existing systems and integrate through APIs, enabling phased modernisation and faster launches.",
  },
  {
    title: "How do you keep governance when moving quickly?",
    description:
      "Arkam supports controlled roles, approval steps where required, and auditable event trails so teams can iterate while maintaining accountability.",
  },
];

const walletAccountItems = [
  {
    title: "Seamless wallet account creation & instant onboarding",
    image: "/images/wallet-account-1.webp",
    color: "dark-blue",
    description:
      "Empower users to initiate their digital banking journey with instant onboarding using institution-defined validation rules for secure, policy-aligned enrollment.",
  },
  {
    title: "Flexible wallet configuration & financial journey entry point",
    image: "/images/wallet-account-2.webp",
    color: "orange",
    description:
      "Wallet accounts can be provisioned as standalone offerings or entry points into broader financial journeys, supporting multi-currency, KYC checks, and low-balance notifications.",
  },
  {
    title: "API-first provisioning with traceability & compliance",
    image: "/images/wallet-account-3.webp",
    color: "light-blue",
    description:
      "Events are logged for customer service traceability and compliance, enabling fintechs to scale wallet offerings across geographies with audit-ready activity logs.",
  },
];
</script>

<style lang="scss" scoped></style>
