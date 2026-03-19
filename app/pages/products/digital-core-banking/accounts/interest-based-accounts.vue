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

  <SectionTextListImage
    title="Savings and Term Deposits, Built on One Deposit Engine"
    description="Design deposit products that match your strategy without rebuilding core logic each time and manage product behavior consistently across channels and back-office processes."
    image="/images/savings-and-term-deposits.webp"
    :items="SavingsAndTermDeposits"
  />

  <SectionTextIconList
    title="Automated Interest Accrual and Posting"
    description="Arkam automates interest calculation based on the rules defined for each product. Interest accrual and posting are executed systematically reducing manual workload, improving accuracy, and ensuring the same logic is applied across every account."
    :items="AutomatedInterest"
  />

  <SectionTextListImage
    title="Interest Credit and Capitalization Aligned to your Policy"
    description="Different products require different treatment of earned interest. Arkam supports configurable interest crediting and capitalization behavior so banks can align deposit products with policy and customer expectations—while maintaining consistent accounting entries and statement visibility."
    image="/images/interestcredit.webp"
    :items="InterestCredit"
  />

  <SectionTextListImageItems :dark="true" :items="AlternateSections" />

  <SectionTextList
    title="Frequently Asked Questions"
    description="Short answers to how Arkam Core fits into your architecture, security model and roadmap."
    :items="faq"
  />
</template>

<script setup>
import HeroTextOnly from "../../../../components/hero/HeroTextOnly.vue";
import SectionTextImageFull from "../../../../components/sections/SectionTextImageFull.vue";
import SectionTextListImage from "../../../../components/sections/SectionTextListImage.vue";
import SectionTextIconList from "../../../../components/sections/SectionTextIconList.vue";
import SectionTextListImageItems from "../../../../components/sections/SectionTextListImageItems.vue";
import SectionTextList from "../../../../components/sections/SectionTextList.vue";

useSeoMeta({
  title: "Arkam - Interest Based Accounts",
  ogTitle: "Arkam - Interest Based Accounts",
  description:
    "Arkam’s Digital Core Banking system supports savings and term-deposit products with configurable interest policies. Banks define accrual and capitalization rules at product level, and the platform executes them automatically keeping balances accurate, statements clear, and reporting consistent for operations and finance teams, without custom code for each variation.",
  ogDescription:
    "Arkam’s Digital Core Banking system supports savings and term-deposit products with configurable interest policies. Banks define accrual and capitalization rules at product level, and the platform executes them automatically keeping balances accurate, statements clear, and reporting consistent for operations and finance teams, without custom code for each variation.",
  // ogImage: "https://example.com/image.png",
  // twitterCard: "summary_large_image",
});

const SavingsAndTermDeposits = [
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

const AutomatedInterest = [
  {
    title: "Configurable Accrual Rules",
    description: "(Define how and when interest accrues)",
  },
  {
    title: "Automated Posting",
    description: "According to product policy",
  },
  {
    title: "Operational Controls and Traceability",
    description: "To support audit and review",
  },
];

const InterestCredit = [
  {
    title: "Configurable Capitalization Rules",
    description: "(How earned interest is applied over time)",
  },
  {
    title: "Clear Posting Events",
    description: "So interest movements are visible and explainable",
  },
  {
    title: "Controlled Behavior by Product",
    description: "not by one-off customization",
  },
];

const RateTables = [
  {
    title: "Rate Configuration per Product",
    description: "(And where applicable, by currency/tenure)",
  },
  {
    title: "Centralized Updates ",
    description: "To keep changes consistent across accounts",
  },
  {
    title: "Governed Change Behavior ",
    description: "That supports controlled rollout and review",
  },
];

const AlternateSections = [
  {
    title: "Rate Tables You Control at Product Level",
    description:
      "Arkam enables banks to manage interest parameters through product configuration, helping teams adjust deposit offerings faster while keeping the underlying execution consistent and controlled.",
    image: "/images/rate-tables.webp",
    items: [
      {
        title: "Rate Configuration per Product",
        description: "(And where applicable, by currency/tenure)",
      },
      {
        title: "Centralized Updates",
        description: "To keep changes consistent across accounts",
      },
      {
        title: "Governed Change Behavior",
        description: "That supports controlled rollout and review",
      },
    ],
  },
  {
    title: "Transparency for Customers, Auditability for the Bank",
    description:
      "Arkam supports statement generation and traceable posting, so interest activity is clear to customers and defensible for internal governance. The platform keeps a consistent record of interest accrual and posting events, supporting operational oversight and reporting needs.",
    image: "/images/transparency-for-customers.webp",
    items: [
      {
        title: "Statement Generation",
        description: "With interest and fee visibility",
      },
      {
        title: "Traceable Posting History",
        description: "For audit and dispute handling",
      },
      {
        title: "Reporting Readiness",
        description: "For finance and operational review",
      },
    ],
  },
];

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
</script>

<style lang="scss" scoped></style>
