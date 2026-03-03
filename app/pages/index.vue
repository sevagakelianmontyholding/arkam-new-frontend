<template>
  <section class="lg:py-16!">
    <div class="container">
      <div class="text-center heading">
        <h1>One Composable Platform for Digital Banking & Super-App Finance</h1>
        <p>
          Arkam unifies core banking, cards, wallets, lending and e-services on
          a cloud-native, API-first platform.
        </p>
        <NuxtLink class="a-button secondary" to="/">Book a live Demo</NuxtLink>
        <img class="w-full" src="~/assets/img/homebanner.webp" />

        <div
          class="flex max-lg:flex-col items-center justify-between lg:gap-16 max-lg:gap-6"
        >
          <div>
            <p class="text-pretty">
              Connect with Our Partners and Collaborators
            </p>
          </div>

          <div class="lg:w-2/3 max-lg:w-full">
            <LogosMarquee />
          </div>
        </div>
      </div>
    </div>
  </section>

  <section class="bg-primary"></section>

  <section>
    <div class="container text-center heading">
      <h2>Arkam Technology</h2>
      <p>
        Arkam Core is built as a cloud-native, microservices-based platform on
        Kubernetes, designed for continuous availability, resilience and scale.
        It is API-first by design, making it easy to integrate with existing
        cores, payment rails and third-party FinTechs.
      </p>
      <NuxtLink to="/" class="a-button tertiary">Book a live Demo</NuxtLink>

      <div class="flex max-lg:flex-col max-lg:gap-8 items-center">
        <div class="w-full">
          <img src="~/assets/img/technology-1.webp" />
        </div>
        <div class="w-full max-lg:hidden">
          <img src="~/assets/img/technology-shape.svg" />
        </div>
        <div class="w-full">
          <img src="~/assets/img/technology-2.webp" />
        </div>
      </div>
    </div>
  </section>

  <section class="bg-[#E6EFE9]">
    <div class="container">
      <div class="heading">
        <h2>Digital Banking Platform</h2>
        <p>
          Ready-made digital experiences for every segment, powered by the same
          composable core.
        </p>
      </div>
    </div>
  </section>

  <HomeTrustedBy />
  <HomeFeaturedInsights />
</template>

<script setup></script>

<style lang="scss" scoped></style>
