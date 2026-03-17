<template>
  <HeroTextImage
    title="Currency Exchange"
    description="Currency exchange logic connects accounts, FX rates and accounting so cross-currency flows are handled consistently. Institutions can apply their chosen FX sources and rules while ensuring that balances and postings remain accurate."
    :button-one="{ link: '/', text: 'Book a Live Demo' }"
    :button-two="{ link: '/', text: 'Contact us' }"
    image="/images/currency-exchange.webp"
  />
  <SectionTextListImage
    title="Key Points"
    :items="keyPoints"
    image="/images/currency-exchange-key-points.webp"
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

const keyPoints = [
  {
    title: "Use of Reference FX Rates",
    description:
      "Consume FX rates from internal treasury systems or approved external sources and apply them consistently across relevant operations.",
  },
  {
    title: "Configurable Conversion Rules",
    description:
      "Define when FX rates are taken, how rounding is handled and how conversions affect customer balances and internal positions.",
  },
  {
    title: "Accounting Impact",
    description:
      "Provide the data needed to reflect FX-related gains, losses and revaluations within the accounting framework, in line with internal policy.",
  },
];

const faq = [
  {
    title:
      "How does Arkam handle currency exchange across accounts and transactions?",
    description:
      "Arkam connects accounts, reference FX rates and accounting so cross-currency flows are handled consistently. Conversions follow configurable rules to keep balances and postings accurate.",
  },
  {
    title: "Can we use our internal treasury FX rates in Arkam?",
    description:
      "Yes. Arkam can consume reference FX rates from internal treasury systems and apply them consistently across relevant operations.",
  },
  {
    title: "Can Arkam also use external FX rate sources?",
    description:
      "Yes. Where required, Arkam can consume FX rates from approved external sources, governed by your institution’s policies and controls.",
  },
  {
    title: "When is the FX rate applied during a conversion?",
    description:
      "Arkam supports configurable conversion rules, including when the FX rate is taken (for example, at initiation or execution), so the institution can align rate timing to policy and operational requirements.",
  },
];
</script>

<style lang="scss" scoped></style>
