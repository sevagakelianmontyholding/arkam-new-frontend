<template>
  <HeroTextOnly
    title="Digital Banking Channels Built for Consistency and Control"
    description="Arkam’s Digital Banking Platform helps institutions deliver a consistent banking experience across every channel—mobile apps, web portals, agent networks, ATMs, POS/QR acceptance and branch teller. Each channel connects to the same core rules for balances, limits, tariffs and approvals, supported by an API-first integration layer so banks can modernise incrementally without disrupting existing systems."
    :button-one="{ link: '/', text: 'Book a Live Demo' }"
    :button-two="{ link: '/', text: 'Contact us' }"
  />
  <SectionTextButtonImage
    title="POS and QR Acceptance"
    description="Enable merchant acceptance journeys through POS and QR, integrated with the institution’s preferred payment rails and acquiring setup. Arkam applies consistent tariffs, limits and posting rules so merchant transactions remain transparent and aligned with finance controls."
    :button-one="{ link: '/', text: 'Book a Live Demo' }"
    :button-two="{ link: '/', text: 'Contact us' }"
    image="/images/pos-and-qr-acceptance.webp"
  />

  <SectionTextListImage
    title="Key Points"
    image="/images/key-points-pos-and-qr-acceptance.webp"
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
  title: "Arkam - POS and QR Acceptance",
  ogTitle: "Arkam - POS and QR Acceptance",
  description:
    "Enable merchant acceptance journeys through POS and QR, integrated with the institution’s preferred payment rails and acquiring setup. Arkam applies consistent tariffs, limits and posting rules so merchant transactions remain transparent and aligned with finance controls.",
  ogDescription:
    "Enable merchant acceptance journeys through POS and QR, integrated with the institution’s preferred payment rails and acquiring setup. Arkam applies consistent tariffs, limits and posting rules so merchant transactions remain transparent and aligned with finance controls.",
  // ogImage: "https://example.com/image.png",
  // twitterCard: "summary_large_image",
});

const whatDoesItEnable = [
  {
    title:
      "Merchant acceptance enablement via POS and QR, integrated through APIs with existing rails or partners.",
  },
  {
    title:
      "Consistent application of fees and tariffs as defined in the pricing catalogue.",
  },
  {
    title:
      "Clear transaction records supporting merchant servicing, exceptions and reporting.",
  },
  {
    title:
      "Multi-currency support where required, aligned with FX rules and accounting treatment.",
  },
  {
    title:
      "Operational controls and audit trails for governance and dispute handling.",
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
