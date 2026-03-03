<template>
  <section>
    <div class="container">
      <div class="heading text-center">
        <h2>Featured Insights</h2>
        <p>
          Practical perspectives on architecture, security and digital banking
          innovation.
        </p>
      </div>

      <div class="flex max-lg:flex-col max-lg:gap-12 mt-16 lg:-mx-6">
        <div
          class="blog-item w-full space-y-5 lg:border-r border-[#C8D3D6] lg:px-6"
          v-for="item in items"
        >
          <NuxtLink
            to="/"
            class="w-full aspect-video relative rounded-2xl overflow-hidden block group"
          >
            <img
              :src="item.thumb"
              class="w-full h-full object-cover absolute top-0 left-0 group-hover:scale-[1.08] transition duration-500"
            />
          </NuxtLink>
          <p class="text-lg">{{ item.date }}</p>
          <NuxtLink to="/" class="block group">
            <h4 class="group-hover:text-secondary!">{{ item.title }}</h4>
          </NuxtLink>
          <p>{{ item.description }}</p>
        </div>
      </div>
      <div class="text-center lg:mt-16 max-lg:mt-8">
        <NuxtLink to="/" class="a-button dark">Learn More</NuxtLink>
      </div>
    </div>
  </section>
</template>

<script setup>
const items = [
  {
    title: "The Composable Core: Launching Products Faster with Microservices",
    description:
      "Separating services like Accounts, Payments and Cards into containerized microservices enables zero-downtime releases and faster speed to market",
    date: "02/01/2026",
    thumb: "/images/blog-1.webp",
  },
  {
    title: "Implementing Zero-Trust: Securing Your Digital Banking Channels",
    description:
      "How Zero-Trust principles, API security and RASP-style protections protect mobile and web banking from evolving threats.",
    date: "02/01/2026",
    thumb: "/images/blog-2.webp",
  },
  {
    title: "Automating AML and KYC with an Integration Hub",
    description:
      "Using Arkam’s Integration Hub and workflow engine to orchestrate KYC, AML and sanction screening at onboarding and during high-risk transactions.",
    date: "02/01/2026",
    thumb: "/images/blog-3.webp",
  },
];
</script>

<style lang="scss" scoped>
.blog-item:last-child {
  border: none;
}
</style>
