<template>
  <div class="relative overflow-hidden bg-background">
    <!-- Fade edges -->
    <div
      class="pointer-events-none absolute inset-0 z-10"
      style="
        background: linear-gradient(
          to right,
          #f9fafc 0%,
          rgba(242, 245, 244, 0) 12%,
          rgba(242, 245, 244, 0) 88%,
          #f9fafc 100%
        );
      "
    />

    <!-- Marquee -->
    <div class="marquee py-6">
      <div class="marquee__inner">
        <!-- Group A -->
        <div class="marquee__group">
          <img
            class="w-auto"
            src="~/assets/img/montycapital.svg"
            alt="Monty Capital"
          />
          <img class="w-auto" src="~/assets/img/mymonty.svg" alt="MyMonty" />
          <img class="w-auto" src="~/assets/img/montypay.svg" alt="MontyPay" />
          <img
            class="w-auto"
            src="~/assets/img/montyfinance.svg"
            alt="Monty Finance"
          />
          <img
            class="w-auto"
            src="~/assets/img/montyesim.svg"
            alt="Monty eSIM"
          />
        </div>

        <!-- Group B (duplicate) -->
        <div class="marquee__group" aria-hidden="true">
          <img class="w-auto" src="~/assets/img/montycapital.svg" alt="" />
          <img class="w-auto" src="~/assets/img/mymonty.svg" alt="" />
          <img class="w-auto" src="~/assets/img/montypay.svg" alt="" />
          <img class="w-auto" src="~/assets/img/montyfinance.svg" alt="" />
          <img class="w-auto" src="~/assets/img/montyesim.svg" alt="" />
        </div>
      </div>
    </div>
  </div>
</template>

<style scoped>
/* tweak these */
.marquee {
  --gap: 4rem; /* spacing between logos */
  --duration: 15s; /* speed */
}

.marquee__inner {
  display: flex;
  width: max-content;
  will-change: transform;
  transform: translate3d(0, 0, 0);
  backface-visibility: hidden;
  animation: marquee var(--duration) linear infinite;
}

/* Make spacing consistent at the seam (start/end) */
.marquee__group {
  display: flex;
  align-items: center;
  gap: var(--gap);
  padding-inline: calc(
    var(--gap) / 2
  ); /* IMPORTANT: same space at the start and end */
}

@keyframes marquee {
  from {
    transform: translate3d(0, 0, 0);
  }
  to {
    transform: translate3d(-50%, 0, 0);
  }
}

@media (prefers-reduced-motion: reduce) {
  .marquee__inner {
    animation: none;
  }
}
</style>
