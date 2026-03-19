<template>
  <HeroTextOnly
    title="Digital Banking Channels Built for Consistency and Control"
    description="Arkam’s Digital Banking Platform helps institutions deliver a consistent banking experience across every channel—mobile apps, web portals, agent networks, ATMs, POS/QR acceptance and branch teller. Each channel connects to the same core rules for balances, limits, tariffs and approvals, supported by an API-first integration layer so banks can modernise incrementally without disrupting existing systems."
    :button-one="{ link: '/', text: 'Book a Live Demo' }"
    :button-two="{ link: '/', text: 'Contact us' }"
  />
  <SectionTextButtonImage
    title="Mobile Banking (Android and iOS)"
    description="Deliver modern retail banking experiences through branded Android and iOS applications. Mobile journeys are powered by the same core services and integration layer, ensuring consistent balances, controls and compliance across the platform."
    :button-one="{ link: '/', text: 'Book a Live Demo' }"
    :button-two="{ link: '/', text: 'Contact us' }"
    image="/images/mobile-banking.webp"
  />

  <SectionTextListImage
    title="Key Points"
    image="/images/key-points-mobile-banking.webp"
    :no-bg="true"
    :items="whatDoesItEnable"
  />

  <SectionTextList
    title="FAQ"
    description="Short answers to how Arkam Core fits into your architecture, security model and roadmap."
    :items="faq"
  />

  <SectionCTABanner
    title="See Arkam Digital Channels in Action"
    description="Explore how Arkam can deliver consistent digital and operational channels on top of a single composable core—with integration-first delivery, governed controls and audit-ready reporting."
    :button-one="{ link: '/', text: 'Book a Live Demo' }"
    :button-two="{ link: '/', text: 'Contact us' }"
  />
</template>

<script setup>
import SectionTextButtonImage from "../../../components/sections/SectionTextButtonImage.vue";
import SectionTextListImage from "../../../components/sections/SectionTextListImage.vue";
import SectionTextList from "../../../components/sections/SectionTextList.vue";
import SectionCTABanner from "../../../components/sections/SectionCTABanner.vue";
import HeroTextOnly from "../../../components/hero/HeroTextOnly.vue";

useSeoMeta({
  title: "Arkam - Mobile Banking (Android and iOS)",
  ogTitle: "Arkam - Mobile Banking (Android and iOS)",
  description:
    "Deliver modern retail banking experiences through branded Android and iOS applications. Mobile journeys are powered by the same core services and integration layer, ensuring consistent balances, controls and compliance across the platform.",
  ogDescription:
    "Deliver modern retail banking experiences through branded Android and iOS applications. Mobile journeys are powered by the same core services and integration layer, ensuring consistent balances, controls and compliance across the platform.",
  // ogImage: "https://example.com/image.png",
  // twitterCard: "summary_large_image",
});

const whatDoesItEnable = [
  {
    title:
      "Digital onboarding journeys with configurable checks and approvals aligned to local policy.",
  },
  {
    title:
      "Account and wallet views with real-time balances, transaction history and downloadable statements.",
  },
  {
    title:
      "Self-service controls (profile updates, channel controls, and customer-initiated service requests) governed by policy.",
  },
  {
    title:
      "Alerts and notifications to keep customers informed about important account events and actions.",
  },
  {
    title:
      "Secure session handling aligned with the institution’s authentication and identity stack.",
  },
];

const faq = [
  {
    title: "Can we launch channels gradually without a big-bang migration?",
    description:
      "Yes. Arkam is designed for phased rollout. Channels can be deployed alongside existing systems and integrated through APIs, so institutions can modernise incrementally.",
  },
  {
    title: "Do all channels share the same balances, limits and controls?",
    description:
      "Yes. Channels connect to the same core services and policy rules, helping ensure consistent balances, limits, tariffs and account status across mobile, web and operational servicing tools.",
  },
  {
    title:
      "Is the channel layer secure and aligned with regulated environments?",
    description:
      "Arkam supports integration with existing authentication and identity services, and applies auditability and governance controls suited to regulated deployment models.",
  },
];
</script>

<style lang="scss" scoped></style>
