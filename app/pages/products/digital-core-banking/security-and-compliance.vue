<template>
  <HeroTextImage
    title="Security and Compliance"
    description="Security and compliance expectations reach all the way into the core. Arkam incorporates access control, auditability and integration points with compliance tools so account-related processes can be governed and monitored effectively, aligned with your IT and regulatory frameworks."
    :button-one="{ link: '/', text: 'Book a Live Demo' }"
    :button-two="{ link: '/', text: 'Contact us' }"
    image="/images/security-and-compliance.webp"
  />
  <SectionTextListImage
    title="Key Points"
    :items="keyPoints"
    image="/images/security-key-points.webp"
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
import SectionCTABanner from "../../../components/sections/SectionCTABanner.vue";
import ArkamCoreBankingInAction from "../../../components/ArkamCoreBankingInAction.vue";

const keyPoints = [
  {
    title: "Role-Based Access Control",
    description:
      "Separate operational, finance, administrative and audit functions using granular roles and permissions aligned with internal policies.",
  },
  {
    title: "Support for Strong Authentication",
    description:
      "Integrate Arkam with existing authentication and identity services, including stronger factors for sensitive operations where required.",
  },
  {
    title: "Operational Logging",
    description:
      "Log sensitive operations—such as manual postings, limit changes and account status updates—for review by authorised teams.",
  },
  {
    title: "Compliance Integrations",
    description:
      "Connect account workflows to KYC, AML and sanctions-screening solutions through the integration layer, so key steps follow defined policies.",
  },
  {
    title: "Regulatory Alignment",
    description:
      "IT and security controls are designed to support alignment with central-bank and financial-sector requirements, including documented support for relevant circulars in regulated markets.",
  },
];

const faq = [
  {
    title:
      "How does Arkam enforce access control in the core banking platform?",
    description:
      "Arkam uses role-based access control (RBAC) with granular roles and permissions to separate operational, finance, administrative and audit functions, aligned with internal policies.",
  },
  {
    title:
      "Can Arkam integrate with our existing identity and authentication systems?",
    description:
      "Yes. Arkam is designed to integrate with existing identity and authentication services, including support for stronger authentication factors for sensitive operations where required.",
  },
  {
    title: "What operational activities are logged for governance and audit?",
    description:
      "Arkam logs sensitive operations such as manual postings, limit changes and account status updates, enabling authorised teams to review activity and support internal controls.",
  },
  {
    title: "Does Arkam support segregation of duties between teams?",
    description:
      "Yes. RBAC and policy-aligned permissions help organisation enforce segregation of duties across operations, finance, administration and audit roles.",
  },
];
</script>

<style lang="scss" scoped></style>
