<template>
  <HomeBanner />
  <!-- <HomeCoreBanking /> -->
  <HomeTechnology />
  <HomeDBP />
  <HomeTrustedBy />
  <HomeFeaturedInsights />
  <HomePlatform />
  <SectionTextList
    title="Frequently Asked Questions"
    description="Short answers to how Arkam Core fits into your architecture, security model and roadmap."
    :items="faq"
  />
  <div class="container">
    <div class="divider my-0!"></div>
  </div>

  <SectionTextIconList
    title="Interest Credit & Capitalization Aligned to Your Policy"
    description="Different products require different treatment of earned interest. Arkam supports configurable interest crediting and capitalization behavior so banks can align deposit products with policy and customer expectations—while maintaining consistent accounting entries and statement visibility."
    :items="interestCredit"
  />
  <SectionCTABanner
    title="See how Arkam Core fits your digital banking strategy"
    :button-one="{ link: '/', text: 'Bood a Live Demo' }"
  />
</template>

<script setup>
import SectionCTABanner from "../components/sections/SectionCTABanner.vue";
import SectionTextIconList from "../components/sections/SectionTextIconList.vue";
import SectionTextList from "../components/sections/SectionTextList.vue";

useSeoMeta({
  title: "Arkam",
  ogTitle: "Arkam",
  description:
    "One Composable Platform for Digital Banking & Super-App Finance",
  ogDescription:
    "One Composable Platform for Digital Banking & Super-App Finance",
  // ogImage: "https://example.com/image.png",
  // twitterCard: "summary_large_image",
});

const faq = [
  {
    title: "Is Arkam a cloud-only solution?",
    description:
      "No. Arkam is cloud-native, not cloud-only. You can deploy on regulated public clouds, private clouds or on-premises infrastructure.",
  },
  {
    title: "Can Arkam coexist with our existing core banking system?",
    description:
      "Yes. A common approach is to deploy Arkam alongside your existing core and use it as a digital core for new products, brands or segments.",
  },
  {
    title: "How fast can business teams launch a new product?",
    description:
      "Specialized services across accounts, Our low-code product & workflow designer allows clients to configure & launch new or modified products in days or weeks, depending on complexity.",
  },
];

const interestCredit = [
  {
    title: "Integration-First Delivery",
  },
  {
    title: "Phased Rollout (Alongside Legacy Core)",
  },
  {
    title: "Governance + Audibility Emphasis",
  },
];
</script>

<style lang="scss" scoped></style>
