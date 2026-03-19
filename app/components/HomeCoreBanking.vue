<template>
  <section ref="sectionOne" class="bg-dark-bg lg:min-h-screen">
    <div class="container">
      <div
        class="flex max-lg:flex-col-reverse lg:gap-12 max-lg:gap-6 lg:justify-between"
      >
        <div
          ref="clip"
          class="lg:w-[50%] text-white relative lg:h-[75vh] overflow-y-hidden"
        >
          <div
            class="absolute max-lg:hidden h-[94%] top-1/2 -translate-y-1/2 left-1 w-1.5 bg-[#66C3BE]/20"
          ></div>
          <div class="absolute max-lg:hidden top-0 inline-block">
            <svg
              width="14"
              height="13"
              viewBox="0 0 14 13"
              fill="none"
              xmlns="http://www.w3.org/2000/svg"
            >
              <path d="M0 13H14L7 0L0 13Z" fill="#00A6A6" />
            </svg>
          </div>
          <div class="absolute bottom-0 max-lg:hidden inline-block">
            <svg
              width="14"
              height="13"
              viewBox="0 0 14 13"
              fill="none"
              xmlns="http://www.w3.org/2000/svg"
            >
              <path d="M0 0H14L7 13L0 0Z" fill="#00A6A6" />
            </svg>
          </div>
          <div
            class="space-y-12 lg:absolute top-0 right-0 left-0 lg:pl-15"
            ref="scrollOne"
          >
            <div class="feature space-y-6">
              <p class="font-semibold">01</p>
              <div class="icon lg:scale-0">
                <svg
                  width="51"
                  height="50"
                  viewBox="0 0 51 50"
                  fill="none"
                  xmlns="http://www.w3.org/2000/svg"
                >
                  <path
                    d="M34.2333 0.114743C32.605 -0.154745 30.6765 0.0882378 27.5773 0.452725L5.96668 2.99535C2.5647 3.39743 0 6.28006 0 9.70625C3.17803e-07 9.75263 0.00662737 9.79903 0.00662737 9.84321C0.0044185 9.88959 3.17803e-07 9.93598 0 9.98237V28.8319V28.9109C-1.33305e-05 33.267 -2.37525e-05 36.7145 0.362276 39.4109C0.73342 42.1721 1.51761 44.4076 3.28041 46.1704C5.04316 47.9332 7.27867 48.7174 10.0399 49.0885C10.59 49.1614 11.1688 49.2145 11.7828 49.2608V12.9269H6.75733C4.97688 12.9269 3.53438 11.4844 3.53438 9.70617C3.53438 8.07366 4.75815 6.69746 6.37957 6.50528L27.9905 3.9649C31.3463 3.56949 32.6473 3.43474 33.6569 3.60042C36.5639 4.08421 38.9364 6.19604 39.7559 9.028C39.9834 9.81439 40.0409 10.8151 40.0541 12.9269L43.591 13.7972C43.5888 11.1905 43.5645 9.47408 43.1514 8.04487C41.9514 3.9054 38.4834 0.821629 34.2333 0.114743Z"
                    fill="#B2DDDB"
                  />
                  <foreignObject x="11" y="9" width="43.3444" height="44.5242"
                    ><div
                      xmlns="http://www.w3.org/1999/xhtml"
                      style="
                        backdrop-filter: blur(2px);
                        clip-path: url(#bgblur_0_2146_6370_clip_path);
                        height: 100%;
                        width: 100%;
                      "
                    ></div
                  ></foreignObject>
                  <path
                    data-figma-bg-blur-radius="4"
                    d="M45.3697 14.8865C44.7136 14.4491 44.0178 14.1244 43.2733 13.8703C42.0083 13.3516 41.2244 13.1677 39.7365 13H15V49.4866C16.5949 49.5175 18.3577 49.5242 20.3016 49.5242H32.0823H32.1833C35.4073 49.5242 37.9642 49.5242 40.004 49.3165C42.0959 49.1023 43.841 48.656 45.3697 47.6354C46.5912 46.8203 47.6405 45.7711 48.4557 44.5495C49.4762 43.0208 49.9247 41.2757 50.1367 39.1837C50.3444 37.1438 50.3444 34.5872 50.3444 31.3633V31.2621V31.1611C50.3444 27.9371 50.3444 25.3801 50.1367 23.3382C49.9247 21.2485 49.4762 19.5033 48.4557 17.9747C47.6405 16.7531 46.5913 15.7038 45.3697 14.8865Z"
                    fill="url(#paint0_linear_2146_6370)"
                    fill-opacity="0.5"
                  />
                  <defs>
                    <clipPath
                      id="bgblur_0_2146_6370_clip_path"
                      transform="translate(-11 -9)"
                    >
                      <path
                        d="M45.3697 14.8865C44.7136 14.4491 44.0178 14.1244 43.2733 13.8703C42.0083 13.3516 41.2244 13.1677 39.7365 13H15V49.4866C16.5949 49.5175 18.3577 49.5242 20.3016 49.5242H32.0823H32.1833C35.4073 49.5242 37.9642 49.5242 40.004 49.3165C42.0959 49.1023 43.841 48.656 45.3697 47.6354C46.5912 46.8203 47.6405 45.7711 48.4557 44.5495C49.4762 43.0208 49.9247 41.2757 50.1367 39.1837C50.3444 37.1438 50.3444 34.5872 50.3444 31.3633V31.2621V31.1611C50.3444 27.9371 50.3444 25.3801 50.1367 23.3382C49.9247 21.2485 49.4762 19.5033 48.4557 17.9747C47.6405 16.7531 46.5913 15.7038 45.3697 14.8865Z"
                      />
                    </clipPath>
                    <linearGradient
                      id="paint0_linear_2146_6370"
                      x1="32.6722"
                      y1="13"
                      x2="18.5"
                      y2="50"
                      gradientUnits="userSpaceOnUse"
                    >
                      <stop stop-color="#66C3BE" stop-opacity="0.3" />
                      <stop
                        offset="1"
                        stop-color="#66C3BE"
                        stop-opacity="0.6"
                      />
                    </linearGradient>
                  </defs>
                </svg>
              </div>
              <h5 class="text-3xl max-lg:text-2xl">Accounts & Wallets</h5>
              <p>
                Create and manage current, savings and wallet accounts in real
                time. Support multi-currency balances, instant posting and rich
                transaction history, with limits and controls you can tailor by
                segment and product.
              </p>
            </div>

            <div class="feature space-y-6">
              <p class="font-semibold">02</p>
              <div class="icon lg:scale-0">
                <svg
                  width="50"
                  height="41"
                  viewBox="0 0 50 41"
                  fill="none"
                  xmlns="http://www.w3.org/2000/svg"
                >
                  <foreignObject
                    x="-3.99988"
                    y="12.0662"
                    width="57.3517"
                    height="32.1013"
                    ><div
                      xmlns="http://www.w3.org/1999/xhtml"
                      style="
                        backdrop-filter: blur(2px);
                        clip-path: url(#bgblur_0_2146_10054_clip_path);
                        height: 100%;
                        width: 100%;
                      "
                    ></div
                  ></foreignObject>
                  <path
                    data-figma-bg-blur-radius="4"
                    fill-rule="evenodd"
                    clip-rule="evenodd"
                    d="M49.3324 16.0663C49.3453 17.3079 49.3518 18.6464 49.3518 20.0839C49.3518 24.3641 49.3539 27.7468 48.9989 30.3894C48.6589 32.9114 47.9681 34.9815 46.4682 36.6469L46.1562 36.974C44.439 38.6913 42.2612 39.4552 39.5714 39.8167C36.9289 40.1718 33.5458 40.1675 29.266 40.1675H20.086C15.8058 40.1675 12.4231 40.1718 9.78049 39.8167C7.09061 39.4552 4.9129 38.6913 3.19572 36.974C1.4785 35.2568 0.71458 33.0791 0.353032 30.3893C-0.00203174 27.7467 0.00012238 24.3636 0.00012238 20.0838C0.00012238 18.6463 0.00657809 17.3078 0.0194898 16.0662L49.3324 16.0663Z"
                    fill="url(#paint0_linear_2146_10054)"
                    fill-opacity="0.5"
                  />
                  <path
                    d="M29.266 0.000140055C33.5461 0.000140055 36.9289 -0.0041642 39.5715 0.350901C42.2614 0.712422 44.4391 1.47637 46.1562 3.19359L46.4683 3.52068C47.9682 5.18624 48.6589 7.25637 48.999 9.77822C49.1152 10.6454 49.1883 11.5923 49.2421 12.6231H0.109497C0.163295 11.5923 0.23646 10.6455 0.352665 9.77822C0.714185 7.08835 1.47813 4.91063 3.19536 3.19346C4.91259 1.47623 7.0903 0.712312 9.78012 0.350764C12.4227 -0.0043002 15.8057 2.40902e-06 20.0856 2.40902e-06L29.266 0.000140055Z"
                    fill="#B2DDDB"
                  />
                  <defs>
                    <clipPath
                      id="bgblur_0_2146_10054_clip_path"
                      transform="translate(3.99988 -12.0662)"
                    >
                      <path
                        fill-rule="evenodd"
                        clip-rule="evenodd"
                        d="M49.3324 16.0663C49.3453 17.3079 49.3518 18.6464 49.3518 20.0839C49.3518 24.3641 49.3539 27.7468 48.9989 30.3894C48.6589 32.9114 47.9681 34.9815 46.4682 36.6469L46.1562 36.974C44.439 38.6913 42.2612 39.4552 39.5714 39.8167C36.9289 40.1718 33.5458 40.1675 29.266 40.1675H20.086C15.8058 40.1675 12.4231 40.1718 9.78049 39.8167C7.09061 39.4552 4.9129 38.6913 3.19572 36.974C1.4785 35.2568 0.71458 33.0791 0.353032 30.3893C-0.00203174 27.7467 0.00012238 24.3636 0.00012238 20.0838C0.00012238 18.6463 0.00657809 17.3078 0.0194898 16.0662L49.3324 16.0663Z"
                      />
                    </clipPath>
                    <linearGradient
                      id="paint0_linear_2146_10054"
                      x1="25.0001"
                      y1="16"
                      x2="29.6699"
                      y2="35.4365"
                      gradientUnits="userSpaceOnUse"
                    >
                      <stop stop-color="#B2DDDB" stop-opacity="0.6" />
                      <stop
                        offset="1"
                        stop-color="#B2DDDB"
                        stop-opacity="0.3"
                      />
                    </linearGradient>
                  </defs>
                </svg>
              </div>
              <h5 class="text-3xl max-lg:text-2xl">Payments & Cards</h5>
              <p>
                Process domestic and cross-border payments, issue physical and
                virtual cards, and control limits, PIN, blocks and alerts
                instantly. Connect to existing schemes and payment rails through
                Arkam’s API-first integration hub.
              </p>
            </div>

            <div class="feature space-y-6">
              <p class="font-semibold">03</p>
              <div class="icon lg:scale-0">
                <svg
                  width="50"
                  height="50"
                  viewBox="0 0 50 50"
                  fill="none"
                  xmlns="http://www.w3.org/2000/svg"
                >
                  <path
                    d="M35.5 21C43.5081 21 50 27.4919 50 35.5C50 43.5081 43.5081 50 35.5 50C27.4919 50 21 43.5081 21 35.5C21 27.4919 27.4919 21 35.5 21ZM35.4639 27.2676C34.6289 27.2676 33.9512 27.9433 33.9512 28.7783V28.998C33.7702 29.0634 33.5907 29.1401 33.4141 29.2295L33.3291 29.2705C32.5684 29.652 31.9343 30.2388 31.4961 30.9668C30.09 33.3104 31.4872 36.3339 34.1816 36.7832L36.2461 37.126C36.839 37.2263 37.1463 37.8908 36.8369 38.4053C36.6952 38.6407 36.4925 38.833 36.2461 38.9551L36.1611 38.999C35.9935 39.0817 35.8192 39.1357 35.6406 39.1641C35.584 39.1575 35.5249 39.1533 35.4639 39.1533C35.3746 39.1533 35.2853 39.1606 35.1982 39.1758C34.7993 39.1365 34.4149 38.9615 34.1162 38.665L33.5605 38.1113C32.9697 37.5205 32.0146 37.5205 31.4238 38.1113C30.8331 38.7 30.8331 39.6572 31.4238 40.248L31.9775 40.8037C32.5422 41.3684 33.223 41.7696 33.9512 41.9941V42.1514C33.9513 42.9863 34.6289 43.6621 35.4639 43.6621C36.2988 43.6621 36.9765 42.9863 36.9766 42.1514V41.9307C37.1574 41.8653 37.3363 41.7895 37.5127 41.7002L37.5986 41.6582C38.3593 41.2767 38.9935 40.6899 39.4316 39.9619C40.8353 37.6183 39.4404 34.5948 36.7461 34.1455L34.6787 33.8037C34.0858 33.7033 33.7806 33.0379 34.0879 32.5234C34.2274 32.288 34.4353 32.0967 34.6816 31.9746L34.7666 31.9307C34.9344 31.8479 35.1085 31.793 35.2871 31.7646C35.3438 31.7712 35.4028 31.7754 35.4639 31.7754C35.5532 31.7754 35.6426 31.7692 35.7275 31.7539C36.1265 31.7931 36.5128 31.9672 36.8115 32.2637L37.3672 32.8184C37.958 33.4089 38.9132 33.409 39.5039 32.8184C40.0946 32.2298 40.0944 31.2725 39.5039 30.6816L38.9473 30.125C38.3827 29.5606 37.7046 29.1591 36.9766 28.9346V28.7783C36.9766 27.9433 36.2989 27.2676 35.4639 27.2676Z"
                    fill="#B2DDDB"
                  />
                  <path
                    fill-rule="evenodd"
                    clip-rule="evenodd"
                    d="M35.464 20.9298C43.4915 20.9298 49.9991 27.4375 49.9991 35.4649C49.9991 43.4923 43.4915 50 35.464 50C27.4366 50 20.929 43.4923 20.929 35.4649C20.929 27.4375 27.4366 20.9298 35.464 20.9298ZM35.464 24.4181C29.3638 24.4181 24.4172 29.3648 24.4172 35.4649C24.4172 41.565 29.364 46.5118 35.464 46.5118C41.5641 46.5118 46.5109 41.565 46.5109 35.4649C46.5109 29.3648 41.5641 24.4181 35.464 24.4181Z"
                    fill="#B2DDDB"
                  />
                  <foreignObject x="-4" y="-4" width="47.5348" height="53.3478"
                    ><div
                      xmlns="http://www.w3.org/1999/xhtml"
                      style="
                        backdrop-filter: blur(2px);
                        clip-path: url(#bgblur_0_2146_10083_clip_path);
                        height: 100%;
                        width: 100%;
                      "
                    ></div
                  ></foreignObject>
                  <path
                    data-figma-bg-blur-radius="4"
                    fill-rule="evenodd"
                    clip-rule="evenodd"
                    d="M21.5112 0.000320562C25.2981 0.000320562 28.3152 -0.00185946 30.6744 0.314263C33.0834 0.639105 35.0674 1.32585 36.6395 2.89556C38.2092 4.46745 38.896 6.4514 39.2208 8.86074C39.537 11.2197 39.5348 14.237 39.5348 18.0239V18.2747C37.8866 17.7362 36.1294 17.4418 34.3024 17.4418C24.9907 17.4418 17.4411 24.9915 17.4411 34.3032C17.4411 38.5283 19.0021 42.387 21.5703 45.3456C21.5506 45.3456 21.531 45.3478 21.5114 45.3478H18.0232C14.2362 45.3478 11.2191 45.3521 8.85995 45.036C6.59912 44.7308 4.71329 44.1072 3.19393 42.7359L2.89524 42.4525C1.32553 40.8828 0.638768 38.8988 0.313942 36.4896C-0.00218185 34.1284 4.04713e-07 31.1133 4.04713e-07 27.3264V18.0236C4.04713e-07 14.2367 -0.00217962 11.2196 0.313942 8.86042C0.638784 6.45136 1.32553 4.46741 2.89524 2.89524C4.46713 1.32553 6.45108 0.638768 8.86042 0.313942C11.2194 -0.00218185 14.2367 4.04713e-07 18.0236 4.04713e-07L21.5112 0.000320562ZM9.88442 25.5823C8.92077 25.5823 8.1403 26.3628 8.1403 27.3264C8.1403 28.2879 8.92077 29.0705 9.88442 29.0705H16.8609C17.8224 29.0705 18.605 28.2879 18.605 27.3264C18.605 26.3628 17.8224 25.5823 16.8609 25.5823H9.88442ZM9.88442 18.6058C8.92077 18.6058 8.1403 19.3863 8.1403 20.3499C8.1403 21.3114 8.92077 22.094 9.88442 22.094H21.5112C22.4748 22.094 23.2553 21.3114 23.2553 20.3499C23.2553 19.3863 22.4748 18.6058 21.5112 18.6058H9.88442ZM9.88442 11.6293C8.92077 11.6293 8.1403 12.4098 8.1403 13.3734C8.1403 14.3349 8.92077 15.1175 9.88442 15.1175H28.4876C29.4513 15.1175 30.2318 14.3349 30.2318 13.3734C30.2318 12.4098 29.4513 11.6293 28.4876 11.6293H9.88442Z"
                    fill="url(#paint0_linear_2146_10083)"
                    fill-opacity="0.5"
                  />
                  <defs>
                    <clipPath
                      id="bgblur_0_2146_10083_clip_path"
                      transform="translate(4 4)"
                    >
                      <path
                        fill-rule="evenodd"
                        clip-rule="evenodd"
                        d="M21.5112 0.000320562C25.2981 0.000320562 28.3152 -0.00185946 30.6744 0.314263C33.0834 0.639105 35.0674 1.32585 36.6395 2.89556C38.2092 4.46745 38.896 6.4514 39.2208 8.86074C39.537 11.2197 39.5348 14.237 39.5348 18.0239V18.2747C37.8866 17.7362 36.1294 17.4418 34.3024 17.4418C24.9907 17.4418 17.4411 24.9915 17.4411 34.3032C17.4411 38.5283 19.0021 42.387 21.5703 45.3456C21.5506 45.3456 21.531 45.3478 21.5114 45.3478H18.0232C14.2362 45.3478 11.2191 45.3521 8.85995 45.036C6.59912 44.7308 4.71329 44.1072 3.19393 42.7359L2.89524 42.4525C1.32553 40.8828 0.638768 38.8988 0.313942 36.4896C-0.00218185 34.1284 4.04713e-07 31.1133 4.04713e-07 27.3264V18.0236C4.04713e-07 14.2367 -0.00217962 11.2196 0.313942 8.86042C0.638784 6.45136 1.32553 4.46741 2.89524 2.89524C4.46713 1.32553 6.45108 0.638768 8.86042 0.313942C11.2194 -0.00218185 14.2367 4.04713e-07 18.0236 4.04713e-07L21.5112 0.000320562ZM9.88442 25.5823C8.92077 25.5823 8.1403 26.3628 8.1403 27.3264C8.1403 28.2879 8.92077 29.0705 9.88442 29.0705H16.8609C17.8224 29.0705 18.605 28.2879 18.605 27.3264C18.605 26.3628 17.8224 25.5823 16.8609 25.5823H9.88442ZM9.88442 18.6058C8.92077 18.6058 8.1403 19.3863 8.1403 20.3499C8.1403 21.3114 8.92077 22.094 9.88442 22.094H21.5112C22.4748 22.094 23.2553 21.3114 23.2553 20.3499C23.2553 19.3863 22.4748 18.6058 21.5112 18.6058H9.88442ZM9.88442 11.6293C8.92077 11.6293 8.1403 12.4098 8.1403 13.3734C8.1403 14.3349 8.92077 15.1175 9.88442 15.1175H28.4876C29.4513 15.1175 30.2318 14.3349 30.2318 13.3734C30.2318 12.4098 29.4513 11.6293 28.4876 11.6293H9.88442Z"
                      />
                    </clipPath>
                    <linearGradient
                      id="paint0_linear_2146_10083"
                      x1="19.7674"
                      y1="0"
                      x2="0.799345"
                      y2="44.6139"
                      gradientUnits="userSpaceOnUse"
                    >
                      <stop stop-color="#B2DDDB" stop-opacity="0.3" />
                      <stop
                        offset="1"
                        stop-color="#B2DDDB"
                        stop-opacity="0.6"
                      />
                    </linearGradient>
                  </defs>
                </svg>
              </div>
              <h5 class="text-3xl max-lg:text-2xl">Fees, FX & Accounting</h5>
              <p>
                Design tariffs once and apply them everywhere—fees, commissions,
                FX and interest. The multi-currency engine posts every event to
                the general ledger with full audit trails, giving finance
                accurate, real-time positions and reports.
              </p>
            </div>
          </div>
        </div>
        <div class="lg:w-[40%]">
          <div class="heading">
            <h2>Core Banking Products and Services</h2>
            <p>
              Everything you need to run modern accounts, payments, lending and
              revenue—on one composable core.
            </p>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
import { ref, onMounted, onUnmounted, nextTick } from "vue";
import gsap from "gsap";
import { ScrollTrigger } from "gsap/ScrollTrigger";

gsap.registerPlugin(ScrollTrigger);

const clip = ref(null);
const sectionOne = ref(null);
const scrollOne = ref(null);

let mm = null;
let ctx = null;
let observer = null;
let resizeTimer = null;
let initTimer = null;

function clearInlineStyles() {
  const icons = sectionOne.value
    ? Array.from(sectionOne.value.querySelectorAll(".icon"))
    : [];

  gsap.set([scrollOne.value, ...icons].filter(Boolean), {
    clearProps: "all",
  });
}

function killOwnScrollTriggers() {
  const section = sectionOne.value;
  if (!section) return;

  ScrollTrigger.getAll().forEach((st) => {
    const trigger = st.trigger;
    const pin = st.pin;

    if (trigger === section || pin === section) {
      st.kill();
    }
  });
}

function cleanup() {
  clearTimeout(resizeTimer);
  clearTimeout(initTimer);
  window.removeEventListener("resize", handleResize);

  observer?.disconnect();
  observer = null;

  killOwnScrollTriggers();
  ctx?.revert();
  mm?.revert();

  ctx = null;
  mm = null;
}

function getMetrics() {
  const wrap = clip.value;
  const el = scrollOne.value;

  if (!wrap || !el) {
    return {
      wrapH: 0,
      elH: 0,
      distance: 0,
      startY: 0,
      endY: 0,
    };
  }

  const wrapH = wrap.clientHeight;
  const elH = el.scrollHeight;
  const distance = Math.max(0, elH - wrapH);
  const startY = wrapH;
  const endY = wrapH - elH;

  return { wrapH, elH, distance, startY, endY };
}

function initDesktop() {
  const section = sectionOne.value;
  const wrap = clip.value;
  const el = scrollOne.value;

  if (!section || !wrap || !el) return;

  killOwnScrollTriggers();
  observer?.disconnect();
  observer = null;
  ctx?.revert();

  ctx = gsap.context((self) => {
    const icons = self.selector(".icon");
    const features = self.selector(".feature");

    ScrollTrigger.saveStyles([el, ...icons]);

    const initial = getMetrics();
    gsap.set(el, { y: initial.startY });
    gsap.set(icons, { scale: 0 });

    ScrollTrigger.create({
      trigger: section,
      start: "top top",
      end: () => {
        const { distance } = getMetrics();
        return `+=${distance + window.innerHeight * 0.35}`;
      },
      pin: true,
      scrub: 1,
      anticipatePin: 1,
      invalidateOnRefresh: true,
      refreshPriority: 2,
      onUpdate: (self) => {
        const { startY, endY } = getMetrics();
        const y = startY + (endY - startY) * self.progress;
        gsap.set(el, { y });
      },
      onRefreshInit: () => {
        const { startY } = getMetrics();
        gsap.set(el, { y: startY });
      },
    });

    observer = new IntersectionObserver(
      (entries) => {
        entries.forEach((entry) => {
          const icon = entry.target.querySelector(".icon");
          if (!icon) return;

          if (entry.isIntersecting) {
            gsap.to(icon, {
              scale: 1,
              duration: 0.4,
              ease: "power2.out",
              overwrite: "auto",
            });
          } else {
            gsap.to(icon, {
              scale: 0,
              duration: 0.25,
              ease: "power2.out",
              overwrite: "auto",
            });
          }
        });
      },
      {
        root: wrap,
        threshold: 0.5,
      },
    );

    features.forEach((feature) => observer.observe(feature));
  }, sectionOne.value);

  ScrollTrigger.refresh();
}

function handleResize() {
  clearTimeout(resizeTimer);
  resizeTimer = setTimeout(() => {
    ScrollTrigger.refresh();
  }, 150);
}

onMounted(async () => {
  await nextTick();

  initTimer = setTimeout(() => {
    requestAnimationFrame(() => {
      requestAnimationFrame(() => {
        mm = gsap.matchMedia();

        mm.add("(min-width: 1024px)", () => {
          initDesktop();
          window.addEventListener("resize", handleResize);

          return () => {
            window.removeEventListener("resize", handleResize);
            observer?.disconnect();
            observer = null;
            killOwnScrollTriggers();
            ctx?.revert();
          };
        });

        mm.add("(max-width: 1023px)", () => {
          observer?.disconnect();
          observer = null;
          killOwnScrollTriggers();
          clearInlineStyles();

          return () => {
            clearInlineStyles();
          };
        });

        ScrollTrigger.refresh();
      });
    });
  }, 0);
});

onUnmounted(() => {
  cleanup();
});
</script>

<style lang="scss" scoped>
.icon {
  display: inline-block;
}
</style>
