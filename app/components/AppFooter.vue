<template>
  <footer class="pt-16">
    <div class="container">
      <div
        class="flex justify-between max-lg:flex-col max-lg:gap-8 lg:gap-12 xl:gap-32"
      >
        <div class="space-y-6 lg:w-full xl:w-auto">
          <h4>Stay Ahead of Digital Banking Change</h4>
          <p>
            Get concise insights on digital banking architecture, security and
            product innovation created by Arkam’s delivery teams. No spam.
          </p>
          <div class="flex max-lg:flex-col gap-4">
            <input
              class="border border-[#0B1F2A]/6 rounded-full pt-3 pb-2 px-6 lg:w-2/3 max-lg:w-full"
              type="text"
              placeholder="Enter you email address"
            />
            <button class="a-button tertiary cursor-pointer max-lg:w-full">
              Subscribe
            </button>
          </div>
        </div>
        <div class="flex lg:justify-between max-lg:flex-col gap-6 w-full">
          <div>
            <h5 class="font-bold text-[22px] mb-3">Products</h5>
            <ul class="space-y-2 text-base">
              <li><NuxtLink to="/">Digital Core Banking</NuxtLink></li>
              <li><NuxtLink to="/">Payments & Transfers</NuxtLink></li>
              <li><NuxtLink to="/">Cards & Wallets</NuxtLink></li>
              <li><NuxtLink to="/">Lending & BNPL</NuxtLink></li>
              <li><NuxtLink to="/">Bills & Collections</NuxtLink></li>
              <li>
                <NuxtLink to="/">Digital Channels (Web & Mobile)</NuxtLink>
              </li>
            </ul>
          </div>

          <div>
            <h5 class="font-bold text-[22px] mb-3">Information</h5>
            <ul class="space-y-2 text-base">
              <li><NuxtLink to="/">Architecture & Technology</NuxtLink></li>
              <li><NuxtLink to="/">Security & Compliance</NuxtLink></li>
              <li><NuxtLink to="/">APIs & Integrations</NuxtLink></li>
              <li><NuxtLink to="/">Implementation Approach</NuxtLink></li>
              <li><NuxtLink to="/">Documentation & Downloads</NuxtLink></li>
            </ul>
          </div>

          <div>
            <h5 class="font-bold text-[22px] mb-3">Company</h5>
            <ul class="space-y-2 text-base">
              <li><NuxtLink to="/">About Arkam</NuxtLink></li>
              <li><NuxtLink to="/">Case Studies</NuxtLink></li>
              <li><NuxtLink to="/">Partners</NuxtLink></li>
              <li><NuxtLink to="/">Careers</NuxtLink></li>
              <li><NuxtLink to="/">Contact Sales</NuxtLink></li>
            </ul>
          </div>
        </div>
      </div>

      <div class="divider lg:mt-20! mb-0!"></div>

      <div
        class="flex lg:items-center lg:justify-between max-lg:flex-col gap-6 py-8 max-lg:items-center text-center"
      >
        <Logo />
        <div class="flex max-lg:flex-col gap-6 text-base">
          <NuxtLink to="/">Terms</NuxtLink>
          <NuxtLink to="/">Privacy</NuxtLink>
          <NuxtLink to="/">Cookies</NuxtLink>
        </div>
        <div class="flex items-center gap-3">
          <a
            class="w-[50px] h-[50px] rounded-full bg-tertiary flex items-center justify-center hover:bg-primary"
            href=""
            target="_blank"
            ><svg
              width="29"
              height="29"
              viewBox="0 0 29 29"
              fill="none"
              xmlns="http://www.w3.org/2000/svg"
            >
              <path
                d="M19.214 9.60742C21.125 9.60742 22.9576 10.3665 24.3089 11.7178C25.6601 13.069 26.4193 14.9017 26.4193 16.8127V25.2188H21.6158V16.8127C21.6158 16.1757 21.3627 15.5648 20.9123 15.1144C20.4619 14.664 19.851 14.4109 19.214 14.4109C18.577 14.4109 17.9661 14.664 17.5157 15.1144C17.0653 15.5648 16.8123 16.1757 16.8123 16.8127V25.2188H12.0088V16.8127C12.0088 14.9017 12.7679 13.069 14.1192 11.7178C15.4704 10.3665 17.3031 9.60742 19.214 9.60742V9.60742Z"
                fill="#00A6A6"
              />
              <path
                d="M7.20534 10.8076H2.40186V25.2181H7.20534V10.8076Z"
                fill="#00A6A6"
              />
              <path
                d="M4.8036 7.20486C6.13005 7.20486 7.20534 6.12956 7.20534 4.80311C7.20534 3.47666 6.13005 2.40137 4.8036 2.40137C3.47715 2.40137 2.40186 3.47666 2.40186 4.80311C2.40186 6.12956 3.47715 7.20486 4.8036 7.20486Z"
                fill="#00A6A6"
              />
            </svg>
          </a>

          <a
            class="w-[50px] h-[50px] rounded-full bg-tertiary flex items-center justify-center hover:bg-primary"
            href=""
            target="_blank"
          >
            <svg
              width="14"
              height="25"
              viewBox="0 0 14 25"
              fill="none"
              xmlns="http://www.w3.org/2000/svg"
            >
              <path
                d="M13.2096 0H9.60698C8.01452 0 6.48729 0.6326 5.36125 1.75864C4.23522 2.88467 3.60262 4.4119 3.60262 6.00436V9.60698H0V14.4105H3.60262V24.0174H8.4061V14.4105H12.0087L13.2096 9.60698H8.4061V6.00436C8.4061 5.68587 8.53262 5.38042 8.75783 5.15522C8.98304 4.93001 9.28848 4.80349 9.60698 4.80349H13.2096V0Z"
                fill="#00A6A6"
              />
            </svg>
          </a>

          <a
            class="w-[50px] h-[50px] rounded-full bg-tertiary flex items-center justify-center hover:bg-primary"
            href=""
            target="_blank"
            ><svg
              width="29"
              height="29"
              viewBox="0 0 29 29"
              fill="none"
              xmlns="http://www.w3.org/2000/svg"
            >
              <path
                fill-rule="evenodd"
                clip-rule="evenodd"
                d="M19.8071 1.75H8.97286C4.98378 1.75 1.75 4.98378 1.75 8.97286V19.8071C1.75 23.7961 4.98378 27.03 8.97286 27.03H19.8071C23.7961 27.03 27.03 23.7961 27.03 19.8071V8.97286C27.03 4.98378 23.7961 1.75 19.8071 1.75Z"
                stroke="#00A6A6"
                stroke-width="3.5"
                stroke-linecap="round"
                stroke-linejoin="round"
              />
              <path
                fill-rule="evenodd"
                clip-rule="evenodd"
                d="M14.3903 19.8079C11.3984 19.8079 8.97314 17.3827 8.97314 14.3908C8.97314 11.3989 11.3984 8.97363 14.3903 8.97363C17.3822 8.97363 19.8074 11.3989 19.8074 14.3908C19.8074 15.8274 19.2366 17.2053 18.2208 18.2212C17.2049 19.2371 15.8269 19.8079 14.3903 19.8079Z"
                stroke="#00A6A6"
                stroke-width="3.5"
                stroke-linecap="round"
                stroke-linejoin="round"
              />
              <path
                d="M21.6124 5.3622C20.6151 5.3622 19.8066 6.17065 19.8066 7.16792C19.8066 8.16519 20.6151 8.97363 21.6124 8.97363C22.6096 8.97363 23.4181 8.16519 23.4181 7.16792C23.4181 6.17065 22.6096 5.3622 21.6124 5.3622Z"
                fill="#00A6A6"
              />
              <path
                d="M21.6128 6.2646C21.1142 6.2646 20.71 6.66882 20.71 7.16746C20.71 7.66609 21.1142 8.07031 21.6128 8.07031C22.1115 8.07031 22.5157 7.66609 22.5157 7.16746C22.5157 6.66882 22.1115 6.2646 21.6128 6.2646Z"
                stroke="#00A6A6"
                stroke-width="1.52"
                stroke-linecap="round"
              />
            </svg>
          </a>
        </div>
      </div>
    </div>
  </footer>
</template>

<script setup></script>

<style lang="scss" scoped></style>
