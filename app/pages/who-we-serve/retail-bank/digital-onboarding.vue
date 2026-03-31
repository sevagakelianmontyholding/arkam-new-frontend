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

  <SectionTextImageGrid
    title="Client Enrollment"
    description="Arkam’s enrollment framework allows financial institutions to craft user-friendly digital journeys across web and mobile platforms."
    :button-one="{ link: '/', text: 'Book a Live Demo' }"
    :button-two="{ link: '/', text: 'Contact us' }"
    image="/images/client-enrollment.webp"
    :items="clienEnrollmentItems"
  />

  <SectionTextTabs
    title="Seamless AML, KYC & Screening Integration"
    description="Arkam’s onboarding engine integrates seamlessly with leading AML, KYC, and sanctions-screening platforms to ensure compliance and streamline customer due diligence."
    :tabs="seamlessTabs"
  />

  <SectionImageTextIconList
    image="/images/optical-character-recognition.webp"
    title="Optical Character Recognition (OCR)"
    description="Enhances the document upload experience by extracting data from scanned IDs, utility bills, income proofs, and more."
    :items="opticalCharacterRecognition"
  />

  <SectionTextBannerIconListImage
    title="Liveness Detection"
    description="Liveness and biometric checks serve as critical elements in remote identity verification, especially in mobile-first digital banks."
    :items="livenessDetection"
    image="/images/liveness-detection.webp"
  />

  <SectionTextHalfSlider
    title="Digital Signature"
    description="Electronic signature capability is crucial for capturing consent and authorization in digital banking."
    :sliderItems="sliderItems"
  />

  <SectionTextList
    title="FAQ"
    description="Short answers to how Arkam Core fits into your architecture, security model and roadmap."
    :items="faq"
  />
  <SectionCTABanner
    title="See Retail Journeys Powered by Arkam"
    description="Explore how Arkam can modernise retail customer journeys with consistent core controls, integration-first delivery and operational visibility—from onboarding and accounts to cards, credit and personalised engagement."
    :button-one="{ text: 'Book a Live Demo', link: '/' }"
    :button-two="{ text: 'contact us', link: '/' }"
  />
</template>

<script setup>
import HeroTextImageFullHeight from "../../../components/hero/HeroTextImageFullHeight.vue";
import SectionIconsTextIcons from "../../../components/sections/SectionIconsTextIcons.vue";
import SectionImageTextIconList from "../../../components/sections/SectionImageTextIconList.vue";
import SectionTextBannerIconListImage from "../../../components/sections/SectionTextBannerIconListImage.vue";
import SectionTextHalfSlider from "../../../components/sections/SectionTextHalfSlider.vue";
import SectionTextImageGrid from "../../../components/sections/SectionTextImageGrid.vue";
import SectionTextTabs from "../../../components/sections/SectionTextTabs.vue";
import SectionTextList from "../../../components/sections/SectionTextList.vue";
import SectionCTABanner from "../../../components/sections/SectionCTABanner.vue";

useSeoMeta({
  title: "Arkam - Digital Onboarding That Balances Speed and Compliance",
  ogTitle: "Arkam - Digital Onboarding That Balances Speed and Compliance",
  description:
    "Arkam helps institutions digitise client onboarding without compromising governance. The platform orchestrates onboarding steps and integrates with KYC/AML and identity services so customer enrollment follows defined policies and remains auditable.",
  ogDescription:
    "Arkam helps institutions digitise client onboarding without compromising governance. The platform orchestrates onboarding steps and integrates with KYC/AML and identity services so customer enrollment follows defined policies and remains auditable.",
  // ogImage: "https://example.com/image.png",
  // twitterCard: "summary_large_image",
});

definePageMeta({
  noTopPadding: true,
});

const clienEnrollmentItems = [
  {
    icon: '<svg width="26" height="29" viewBox="0 0 26 29" fill="none" xmlns="http://www.w3.org/2000/svg"><path d="M25 5C25 7.20914 19.6274 9 13 9C6.37258 9 1 7.20914 1 5M25 5C25 2.79086 19.6274 1 13 1C6.37258 1 1 2.79086 1 5M25 5V23.6667C25 25.88 19.6667 27.6667 13 27.6667C6.33333 27.6667 1 25.88 1 23.6667V5M25 11.2936C25 13.507 19.6667 15.2936 13 15.2936C6.33333 15.2936 1 13.507 1 11.2936M25 17.5867C25 19.8 19.6667 21.5867 13 21.5867C6.33333 21.5867 1 19.8 1 17.5867" stroke="#005436" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"/></svg>',
    title: "Smart Data Capture & Validation",
    description:
      "Each flow captures required personal and financial data, integrates with backend systems, and enforces validations to prevent incomplete or inconsistent submissions.",
  },
  {
    icon: '<svg width="29" height="29" viewBox="0 0 29 29" fill="none" xmlns="http://www.w3.org/2000/svg"><path d="M10.3333 14.3333L13 17L19 11M10.6025 25.8012C11.0395 25.7434 11.481 25.8619 11.8291 26.13L13.4334 27.3611C13.9637 27.7685 14.7015 27.7685 15.2303 27.3611L16.8953 26.0826C17.2064 25.8441 17.599 25.7389 17.9871 25.7908L20.0699 26.0649C20.7321 26.1523 21.3705 25.7834 21.6268 25.1656L22.4282 23.2279C22.5778 22.8649 22.8652 22.5776 23.2281 22.4279L25.1658 21.6265C25.7835 21.3717 26.1523 20.7317 26.0649 20.0695L25.8013 18.0621C25.7435 17.6251 25.862 17.1836 26.1301 16.8355L27.3611 15.2311C27.7685 14.7007 27.7685 13.963 27.3611 13.4341L26.0827 11.769C25.8442 11.4579 25.739 11.0653 25.7909 10.6771L26.0649 8.59423C26.1523 7.93203 25.7835 7.29353 25.1658 7.03724L23.2281 6.23578C22.8652 6.08616 22.5778 5.79876 22.4282 5.4358L21.6268 3.49808C21.372 2.88032 20.7321 2.51144 20.0699 2.59884L17.9871 2.87291C17.599 2.92624 17.2064 2.82106 16.8968 2.58403L15.2318 1.30555C14.7015 0.898151 13.9637 0.898151 13.4349 1.30555L11.7698 2.58403C11.4588 2.82106 11.0662 2.92624 10.6781 2.87587L8.59529 2.60181C7.93312 2.5144 7.29466 2.88328 7.03839 3.50104L6.23845 5.43877C6.08735 5.80024 5.79997 6.08764 5.43852 6.23874L3.5009 7.03872C2.88318 7.29501 2.51432 7.93351 2.60172 8.59571L2.87577 10.6786C2.92614 11.0668 2.82096 11.4593 2.58394 11.769L1.30553 13.4341C0.898157 13.9645 0.898157 14.7022 1.30553 15.2311L2.58394 16.8962C2.82244 17.2073 2.92762 17.5999 2.87577 17.988L2.60172 20.071C2.51432 20.7332 2.88318 21.3717 3.5009 21.6279L5.43852 22.4294C5.80145 22.579 6.08883 22.8664 6.23845 23.2294L7.03987 25.1671C7.29466 25.7849 7.93461 26.1537 8.59677 26.0663L10.6025 25.8012Z" stroke="#005436" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"/></svg>',
    title: "Adaptive KYC & Verification Flow",
    description:
      "Identity verification steps, such as document upload, contact verification, and consent acknowledgments, are streamlined for clarity.",
  },
  {
    icon: '<svg width="26" height="29" viewBox="0 0 26 29" fill="none" xmlns="http://www.w3.org/2000/svg"><path d="M13 3.66667V18.6C13 20.8402 13 21.9603 13.436 22.816C13.8195 23.5686 14.4314 24.1805 15.184 24.564C16.0397 25 17.1598 25 19.4 25H19.6667M19.6667 25C19.6667 26.4728 20.8606 27.6667 22.3333 27.6667C23.8061 27.6667 25 26.4728 25 25C25 23.5272 23.8061 22.3333 22.3333 22.3333C20.8606 22.3333 19.6667 23.5272 19.6667 25ZM6.33333 3.66667L19.6667 3.66667M6.33333 3.66667C6.33333 5.13943 5.13943 6.33333 3.66667 6.33333C2.19391 6.33333 1 5.13943 1 3.66667C1 2.19391 2.19391 1 3.66667 1C5.13943 1 6.33333 2.19391 6.33333 3.66667ZM19.6667 3.66667C19.6667 5.13942 20.8606 6.33333 22.3333 6.33333C23.8061 6.33333 25 5.13943 25 3.66667C25 2.19391 23.8061 1 22.3333 1C20.8606 1 19.6667 2.19391 19.6667 3.66667ZM13 14.3333H19.6667M19.6667 14.3333C19.6667 15.8061 20.8606 17 22.3333 17C23.8061 17 25 15.8061 25 14.3333C25 12.8606 23.8061 11.6667 22.3333 11.6667C20.8606 11.6667 19.6667 12.8606 19.6667 14.3333Z" stroke="#005436" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"/></svg>',
    title: "Flexible Onboarding Control",
    description:
      "With centralized configuration, banks can manage review steps, escalation flows, and data enrichment to optimize onboarding performance and customer satisfaction.",
  },
];

const seamlessTabs = [
  {
    title: "AML",
    image: "/images/aml.webp",
  },
  {
    title: "KYC",
    image: "/images/kyc.webp",
  },
  {
    title: "Sanctions Screening",
    image: "/images/sanctions-screening.webp",
  },
];

const opticalCharacterRecognition = [
  {
    icon: '<svg width="26" height="29" viewBox="0 0 26 29" fill="none" xmlns="http://www.w3.org/2000/svg"><path d="M25 5C25 7.20914 19.6274 9 13 9C6.37258 9 1 7.20914 1 5M25 5C25 2.79086 19.6274 1 13 1C6.37258 1 1 2.79086 1 5M25 5V23.6667C25 25.88 19.6667 27.6667 13 27.6667C6.33333 27.6667 1 25.88 1 23.6667V5M25 11.2936C25 13.507 19.6667 15.2936 13 15.2936C6.33333 15.2936 1 13.507 1 11.2936M25 17.5867C25 19.8 19.6667 21.5867 13 21.5867C6.33333 21.5867 1 19.8 1 17.5867" stroke="#005436" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"/></svg>',
    title: "Automated Data Extraction & Validation",
    description:
      "Recognizes structured and unstructured documents, extracts key fields, and validates them against user inputs in real time.",
  },
  {
    icon: '<svg width="48" height="48" viewBox="0 0 48 48" fill="none" xmlns="http://www.w3.org/2000/svg"><g opacity="0.3"><rect x="1" y="1" width="46" height="46" rx="23" stroke="#011520" stroke-width="2"/></g><path d="M24.0001 18.6665V23.9998M24.0001 29.3332H24.0134M37.3334 23.9998C37.3334 31.3636 31.3639 37.3332 24.0001 37.3332C16.6363 37.3332 10.6667 31.3636 10.6667 23.9998C10.6667 16.636 16.6363 10.6665 24.0001 10.6665C31.3639 10.6665 37.3334 16.636 37.3334 23.9998Z" stroke="#011520" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"/></svg>',
    title: "Error Reduction & Faster Onboarding",
    description:
      "Minimizes manual data entry, reduces errors, and accelerates onboarding with secure data mapping and fallback support.",
  },
  {
    icon: '<svg width="26" height="21" viewBox="0 0 26 21" fill="none" xmlns="http://www.w3.org/2000/svg"><path d="M25 10.3333L9 10.3333M25 2.33333L9 2.33333M25 18.3333L9 18.3333M3.66667 10.3333C3.66667 11.0697 3.06971 11.6667 2.33333 11.6667C1.59695 11.6667 1 11.0697 1 10.3333C1 9.59695 1.59695 9 2.33333 9C3.06971 9 3.66667 9.59695 3.66667 10.3333ZM3.66667 2.33333C3.66667 3.06971 3.06971 3.66667 2.33333 3.66667C1.59695 3.66667 1 3.06971 1 2.33333C1 1.59695 1.59695 1 2.33333 1C3.06971 1 3.66667 1.59695 3.66667 2.33333ZM3.66667 18.3333C3.66667 19.0697 3.06971 19.6667 2.33333 19.6667C1.59695 19.6667 1 19.0697 1 18.3333C1 17.597 1.59695 17 2.33333 17C3.06971 17 3.66667 17.597 3.66667 18.3333Z" stroke="#103B50" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"/></svg>',
    title: "Modular & Scalable OCR Deployment",
    description:
      "Applies OCR selectively across products and channels, enabling intelligent, compliant journeys that improve conversion.",
  },
];

const livenessDetection = [
  {
    icon: '<svg width="27" height="26" viewBox="0 0 27 26" fill="none" xmlns="http://www.w3.org/2000/svg"><path d="M7.66667 1H7.4C5.15979 1 4.03969 1 3.18404 1.43597C2.43139 1.81947 1.81947 2.43139 1.43597 3.18404C1 4.03969 1 5.15979 1 7.4V7.66667M7.66667 25H7.4C5.15979 25 4.03969 25 3.18404 24.564C2.43139 24.1805 1.81947 23.5686 1.43597 22.816C1 21.9603 1 20.8402 1 18.6V18.3333M25 7.66667V7.4C25 5.15979 25 4.03969 24.564 3.18404C24.1805 2.43139 23.5686 1.81947 22.816 1.43597C21.9603 1 20.8402 1 18.6 1H18.3333M25 18.3333V18.6C25 20.8402 25 21.9603 24.564 22.816C24.1805 23.5686 23.5686 24.1805 22.816 24.564C21.9603 25 20.8402 25 18.6 25H18.3333M1 13H1.01333M7 13H7.01333M19 13H19.0133M13 13H13.0133M25 13H25.0133" stroke="#103B50" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"/></svg>',
    title: "Advanced Biometric Integration",
    description:
      "Integrates with certified providers for facial recognition, selfie video, and motion-based liveness detection to verify identity against submitted documents.",
  },
  {
    icon: '<svg width="29" height="29" viewBox="0 0 29 29" fill="none" xmlns="http://www.w3.org/2000/svg"><path d="M3.66667 22.3333H1M6.75215 14.7522L4.86654 12.8665M21.9144 14.7522L23.8 12.8665M27.6667 22.3333H25M7.66667 22.3333C7.66667 18.6514 10.6514 15.6667 14.3333 15.6667C18.0152 15.6667 21 18.6514 21 22.3333M27.6667 27.6667H1M19.6667 6.33333L14.3333 1M14.3333 1L9 6.33333M14.3333 1V10.3333" stroke="black" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"/></svg>',
    title: "Risk-Based Decisioning & Review",
    description:
      "Liveness results can be scored, used in onboarding decisions, or flagged for manual review, with flexible policies for high-risk or universal checks.      ",
  },
  {
    icon: '<svg width="29" height="24" viewBox="0 0 29 24" fill="none" xmlns="http://www.w3.org/2000/svg"><path d="M27.6667 9V5.26667C27.6667 3.77319 27.6667 3.02646 27.376 2.45603C27.1204 1.95426 26.7124 1.54631 26.2106 1.29065C25.6402 1 24.8935 1 23.4 1H5.26667C3.77319 1 3.02646 1 2.45603 1.29065C1.95426 1.54631 1.54631 1.95426 1.29065 2.45603C1 3.02646 1 3.77319 1 5.26667V10.0667C1 11.5601 1 12.3069 1.29065 12.8773C1.54631 13.3791 1.95426 13.787 2.45603 14.0427C3.02646 14.3333 3.77319 14.3333 5.26667 14.3333H13M14.3333 7.66667H14.34M21 7.66667H21.0067M7.66667 7.66667H7.67333M24 17V14.6667C24 13.378 22.9553 12.3333 21.6667 12.3333C20.378 12.3333 19.3333 13.378 19.3333 14.6667V17M14.6667 7.66667C14.6667 7.85076 14.5174 8 14.3333 8C14.1492 8 14 7.85076 14 7.66667C14 7.48257 14.1492 7.33333 14.3333 7.33333C14.5174 7.33333 14.6667 7.48257 14.6667 7.66667ZM21.3333 7.66667C21.3333 7.85076 21.1841 8 21 8C20.8159 8 20.6667 7.85076 20.6667 7.66667C20.6667 7.48257 20.8159 7.33333 21 7.33333C21.1841 7.33333 21.3333 7.48257 21.3333 7.66667ZM8 7.66667C8 7.85076 7.85076 8 7.66667 8C7.48257 8 7.33333 7.85076 7.33333 7.66667C7.33333 7.48257 7.48257 7.33333 7.66667 7.33333C7.85076 7.33333 8 7.48257 8 7.66667ZM19.1333 22.3333H24.2C24.9467 22.3333 25.3201 22.3333 25.6053 22.188C25.8562 22.0602 26.0602 21.8562 26.188 21.6053C26.3333 21.3201 26.3333 20.9467 26.3333 20.2V19.1333C26.3333 18.3866 26.3333 18.0132 26.188 17.728C26.0602 17.4771 25.8562 17.2732 25.6053 17.1453C25.3201 17 24.9467 17 24.2 17H19.1333C18.3866 17 18.0132 17 17.728 17.1453C17.4771 17.2732 17.2732 17.4771 17.1453 17.728C17 18.0132 17 18.3866 17 19.1333V20.2C17 20.9467 17 21.3201 17.1453 21.6053C17.2732 21.8562 17.4771 22.0602 17.728 22.188C18.0132 22.3333 18.3866 22.3333 19.1333 22.3333Z" stroke="#103B50" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"/></svg>',
    title: "Secure & Compliant Data Handling",
    description:
      "Ensures secure transmission and storage of biometric data with full audit trails to support compliance and regulatory requirements.",
  },
];

const faq = [
  {
    title:
      "Can we deploy Arkam retail journeys alongside an existing legacy core?",
    description:
      "Yes. A common approach is to launch retail channels and new propositions on Arkam while integrating with existing core and rails through APIs, enabling phased modernisation.",
  },
  {
    title: "Do onboarding and servicing actions remain auditable?",
    description:
      "Yes. Arkam supports governed workflows and auditability, including traceable servicing events and operational logging for sensitive actions.",
  },
  {
    title:
      "Can we integrate with third-party KYC/AML, e-signature and identity providers?",
    description:
      "Yes. Arkam is integration-first and provides integration points so onboarding and compliance checks can connect to approved tools and follow defined policies.",
  },
];

const sliderItems = [
  {
    title:
      "Integration with recognized digital signature platforms (eIDAS, ESIGN, etc.)",
    description:
      "Supports compliant digital signatures for agreements, disclosures, and terms & conditions using OTPs, certificates, or biometric authentication.",
  },
  {
    title: "Secure storage, timestamping & customer profile linkage",
    description:
      "Signed data is timestamped, stored securely, and attached to the customer’s profile for future reference.",
  },
  {
    title: "Flexible delivery across onboarding and channels",
    description:
      "Supports compliant digital signatures for agreements, disclosures, and terms & conditions using OTPs, certificates, or biometric authentication.",
  },
  {
    title: "Full auditability, revocation support & compliance documentation",
    description:
      "Ensures banks meet legal and operational requirements with minimal friction.",
  },
];
</script>

<style lang="scss" scoped></style>
