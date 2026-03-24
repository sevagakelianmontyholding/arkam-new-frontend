<template>
  <HeroTextImageFullHeight
    title="Digital Onboarding That Balances Speed and Compliance"
    description="Arkam helps institutions digitise client onboarding without compromising governance. The platform orchestrates onboarding steps and integrates with KYC/AML and identity services so customer enrollment follows defined policies and remains auditable."
    :button-one="{ link: '/', text: 'Book a Live Demo' }"
    :button-two="{ link: '/', text: 'Contact us' }"
    image="/images/digital-onboarding-banner.webp"
  />

  <SectionIconsTextIcons
    title="Platform Foundation"
    description="All retail journeys are powered by Arkam’s API-first platform. 
The solution is built as a containerised microservices architecture on Kubernetes, with GitOps-driven deployments, enterprise messaging via RabbitMQ, and observability through Prometheus, Grafana Loki and Jaeger. This foundation helps institutions scale safely and maintain operational visibility."
  />
</template>

<script setup>
import HeroTextImageFullHeight from "../../../components/hero/HeroTextImageFullHeight.vue";
import SectionIconsTextIcons from "../../../components/sections/SectionIconsTextIcons.vue";
definePageMeta({
  noTopPadding: true,
});
</script>

<style lang="scss" scoped></style>
