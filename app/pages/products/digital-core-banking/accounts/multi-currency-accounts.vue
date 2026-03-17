<template>
  <HeroTextOnly
    title="Composable Core Banking for Deposits and Financial Control"
    description="Arkam Core Banking unifies deposits, balances, FX, and controls in one flexible, cloud-ready platform — enabling real-time accuracy, faster launches, and smooth modernization without disruption."
    :button-one="{ text: 'Book a Live Demo', link: '/' }"
    :button-two="{ text: 'Contact us', link: '/' }"
  />

  <SectionTextImageFull
    title="Multi-Currency Accounts"
    description="Arkam’s Digital Core Banking system enables banks to manage multi-currency balances with consistent controls across channels, operations and finance. The platform supports global account management, instant IBAN allocation, and account segmentation so institutions can scale cross-border propositions while keeping governance, reporting and auditability intact."
    image="/images/multi-currency-accounts.webp"
  />

  <SectionTextListImageItems :items="AlternateSections" />
</template>

<script setup>
import HeroTextOnly from "../../../../components/hero/HeroTextOnly.vue";
import SectionTextImageFull from "../../../../components/sections/SectionTextImageFull.vue";
import SectionTextListImageItems from "../../../../components/sections/SectionTextListImageItems.vue";

const AlternateSections = [
  {
    title: "Global Account Management Across Currencies and Segments",
    description:
      "Arkam provides a unified way to manage customer accounts that hold multiple currencies. Banks can operate multi-currency propositions without duplicating core logic across channels or back-office tools, ensuring balances, postings and customer views remain consistent.",
    image: "/images/global-account-management.webp",
    itemsGrid: [
      {
        title: "Multi-currency balances under one relationship",
        description: "(Single customer view, multiple currency positions)",
      },
      {
        title: "Consistent posting and balance updates ",
        description:
          "So available balance and transaction history remain aligned across channels",
      },
      {
        title: "Operational controls",
        description:
          "For account status, limits and lifecycle handling, aligned with bank policy",
      },
      {
        title: "Unified statements and reporting inputs",
        description: "That support customer transparency and finance workflows",
      },
    ],
  },
  {
    title: "Instant IBAN Allocation at Onboarding and Product Upgrade",
    description:
      "Arkam supports automated IBAN allocation as part of digital onboarding and account creation flows. The platform assigns identifiers according to the institution’s numbering scheme and governance rules—helping banks reduce manual steps, speed up activation, and keep controls auditable.",
    image: "/images/instant-iban-allocation.webp",
    items: [
      {
        title: "Kept intentionally conservative:",
        description:
          "“instant IBAN allocation” is framed as automated assignment aligned to the bank’s numbering scheme, without claiming universal country coverage.",
      },
    ],
    itemsGrid: [
      {
        title: "Automated IBAN allocation",
        description:
          "when accounts are created through digital or back-office journeys",
      },
      {
        title: "Rule-based assignment",
        description:
          "aligned to bank-defined numbering logic and eligibility conditions",
      },
      {
        title: "Workflow-aligned controls",
        description: "so allocation can follow required checks and approvals",
      },
      {
        title: "Traceable assignment history",
        description: "supporting operations review and audit requirements",
      },
    ],
  },
  {
    title: "Account Segmentation That Keeps Control as You Scale",
    description:
      "Segmentation ensures multi-currency banking remains governed as volumes grow. Arkam enables banks to segment accounts by product, customer type, geography or business line, and apply differentiated rules—without branching the platform or creating duplicate configurations.",
    image: "/images/account-segmentation.webp",
    itemsGrid: [
      {
        title: "Segmentation by Product, Segment, or Market",
        description: "To support differentiated propositions",
      },
      {
        title: "Policy-driven Controls per Segment",
        description:
          "(Limits, eligibility, pricing applicability where relevant)",
      },
      {
        title: "Operational Consistency",
        description:
          "So segmentation rules apply across channels and back-office processes",
      },
      {
        title: "Reporting Clarity",
        description:
          "With segment-aware views that help monitor performance and risk",
      },
    ],
  },
];
</script>

<style lang="scss" scoped></style>
