<template>
  <section>
    <div class="container">
      <div class="flex max-lg:flex-col max-lg:gap-16 lg:gap-24 lg:items-center">
        <div class="lg:w-2/5">
          <div class="heading">
            <h2>Frequently Asked Questions</h2>
            <p>
              Short answers to how Arkam Core fits into your architecture,
              security model and roadmap.
            </p>
          </div>
        </div>

        <div class="space-y-6 lg:w-3/5">
          <div class="space-y-2" v-for="(item, index) in items" :key="index">
            <h4>{{ item.question }}</h4>
            <p>{{ item.answer }}</p>
            <div class="divider" v-if="index + 1 < items.length"></div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
const items = [
  {
    question: "Is Arkam a cloud-only solution?",
    answer:
      "No. Arkam is cloud-native, not cloud-only. You can deploy on regulated public clouds, private clouds or on-premises infrastructure.",
  },
  {
    question: "Can Arkam coexist with our existing core banking system?",
    answer:
      "Yes. A common approach is to deploy Arkam alongside your existing core and use it as a digital core for new products, brands or segments.",
  },
  {
    question: "How fast can business teams launch a new product?",
    answer:
      "Specialized services across accounts, Our low-code product & workflow designer allows clients to configure & launch new or modified products in days or weeks, depending on complexity.",
  },
];
</script>

<style lang="scss" scoped></style>
