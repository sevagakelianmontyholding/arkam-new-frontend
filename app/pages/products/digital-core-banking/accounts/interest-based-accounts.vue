<template>
  <HeroTextOnly
    title="Composable Core Banking for Deposits and Financial Control"
    description="Arkam Core Banking unifies deposits, balances, FX, and controls in one flexible, cloud-ready platform — enabling real-time accuracy, faster launches, and smooth modernization without disruption."
    :button-one="{ text: 'Book a Live Demo', link: '/' }"
    :button-two="{ text: 'Contact us', link: '/' }"
  />

  <SectionTextImageFull
    title="Interest-Based Accounts"
    description="Arkam’s Digital Core Banking system supports savings and term-deposit products with configurable interest policies. Banks define accrual and capitalization rules at product level, and the platform executes them automatically keeping balances accurate, statements clear, and reporting consistent for operations and finance teams, without custom code for each variation."
    image="/images/interest-based-accounts.webp"
  />

  <SectionTextImage
    title="Savings and Term Deposits, Built on One Deposit Engine"
    description="Design deposit products that match your strategy without rebuilding core logic each time and manage product behavior consistently across channels and back-office processes."
    image="/images/savings-and-term-deposits.webp"
    :items="SectionTextImageItems"
  />
</template>

<script setup>
import HeroTextOnly from "../../../../components/hero/HeroTextOnly.vue";
import SectionTextImageFull from "../../../../components/sections/SectionTextImageFull.vue";
import SectionTextImage from "../../../../components/sections/SectionTextImage.vue";

const SectionTextImageItems = [
  {
    title: "Savings and Term Deposits",
    description: "Supported within the core account engine",
  },
  {
    title: "Product Rules by Configuration ",
    description: "(Tenure, eligibility, basic lifecycle handling)",
  },
  {
    title: "Consistent Posting and Balance Updates ",
    description: "Across customer and back-office views",
  },
];
</script>

<style lang="scss" scoped></style>
