<template>
  <HeroTextImage
    title="Tariffs and Fees"
    description="Tariffs and fees are central to how products generate revenue and must be handled transparently. Arkam centralizes fee and interest rules so pricing can be controlled in one place and applied consistently across products and channels."
    :button-one="{ link: '/', text: 'Book a Live Demo' }"
    :button-two="{ link: '/', text: 'Contact us' }"
    image="/images/tariffs-and-fees.webp"
  />
  <SectionTextListImage
    title="Key Points"
    :items="keyPoints"
    image="/images/tariffs-key-points.webp"
    :darkImage="true"
    :no-image-padding="true"
  />

  <SectionTextList
    title="FAQ"
    description="Short answers to how Arkam Core fits into your architecture, security model and roadmap."
    :items="faq"
  />

  <ArkamCoreBankingInAction />
</template>

<script setup>
import HeroTextImage from "../../../components/hero/HeroTextImage.vue";
import SectionTextListImage from "../../../components/sections/SectionTextListImage.vue";
import SectionTextList from "../../../components/sections/SectionTextList.vue";
import ArkamCoreBankingInAction from "../../../components/ArkamCoreBankingInAction.vue";

useSeoMeta({
  title: "Arkam - Tariffs and Fees",
  ogTitle: "Arkam - Tariffs and Fees",
  description:
    "Tariffs and fees are central to how products generate revenue and must be handled transparently. Arkam centralizes fee and interest rules so pricing can be controlled in one place and applied consistently across products and channels.",
  ogDescription:
    "Tariffs and fees are central to how products generate revenue and must be handled transparently. Arkam centralizes fee and interest rules so pricing can be controlled in one place and applied consistently across products and channels.",
  // ogImage: "https://example.com/image.png",
  // twitterCard: "summary_large_image",
});

const keyPoints = [
  {
    title: "Central Tariff Catalogue",
    description:
      "Maintain definitions for fees, commissions, charges and related pricing elements in a single catalogue.",
  },
  {
    title: "Rule-Based Application",
    description:
      "Apply tariffs based on product, segment, channel, geography or other attributes using configuration, not custom code.",
  },
  {
    title: "Alignment with Multi-Currency and Accounting",
    description:
      "Ensure that tariffs and fees are correctly reflected in both customer-facing views",
  },
  {
    title: "Transparent Communication",
    description:
      "Expose fee details in statements and transaction histories in a way that supports customer understanding and regulatory disclosure requirements.",
  },
];

const faq = [
  {
    title: "How does Arkam manage tariffs and fees across products?",
    description:
      "Arkam centralises tariffs in a single catalogue for fees, commissions and charges. Pricing rules are defined once and applied consistently across products and channels.",
  },
  {
    title: "Can we configure different fees by product or customer segment?",
    description:
      "Yes. Arkam supports rule-based application of tariffs based on attributes such as product, customer segment, channel, geography, or other bank-defined criteria—through configuration rather than custom code.",
  },
  {
    title:
      "Can we apply different pricing by channel (e.g., mobile vs. branch)?",
    description:
      "Yes. Tariffs can be configured to vary by channel so the same product can follow distinct pricing rules depending on where and how it is used.",
  },
  {
    title: "How does Arkam ensure fees are reflected correctly in accounting?",
    description:
      "Arkam aligns tariff application with the accounting layer so charges are reflected consistently in both customer-facing views and the general ledger, supporting accurate financial control.",
  },
];
</script>

<style lang="scss" scoped></style>
