<script setup>
import { ref } from "vue"
import JoinOurCommunityPopUp from "./JoinOurCommunityPopUp.vue"
import ContactPopUp from "./ContactPopUp.vue"

const showMobile = ref(false)
const showCommunityPopUp = ref(false)
const showContactPopUp = ref(false)

function toggleMobile() {
  showMobile.value === true
    ? (showMobile.value = false)
    : (showMobile.value = true)
}

function toggleCommunityPopUp() {
  showCommunityPopUp.value === true
    ? (showCommunityPopUp.value = false)
    : (showCommunityPopUp.value = true)
}

function toggleContactPopUp() {
  showContactPopUp.value === true
    ? (showContactPopUp.value = false)
    : (showContactPopUp.value = true)
}
</script>

<template>
  <header
    class="w-full md:h-[6.3125rem] center fixed z-20 inset-x-0 !bg-[#FFFCF9] flex items-center px-5 md:px-0 h-14"
  >
    <nav
      class="container md:px-[9.375rem] mx-auto flex items-center justify-between h-full"
    >
      <a href="/" class="">
        <img
          src="/codelrlogo.png"
          alt="codelr africa logo"
          class="w-20 md:w-40"
        />
      </a>
      <!-- nav links -->
      <div class="hidden lg:flex items-center gap-7">
        <!-- with dropdown -->
        <!-- <div class="relative group cursor-pointer mr-2"> -->
          <!-- <div class="flex items-center gap-2">
            <p class="text-base font-medium">Schools</p>
            <svg
              xmlns="http://www.w3.org/2000/svg"
              viewBox="0 0 512 512"
              width="15"
              height="15"
              class="group-hover:rotate-180 duration-300"
            >
              <path
                d="M233.4 406.6c12.5 12.5 32.8 12.5 45.3 0l192-192c12.5-12.5 12.5-32.8 0-45.3s-32.8-12.5-45.3 0L256 338.7 86.6 169.4c-12.5-12.5-32.8-12.5-45.3 0s-12.5 32.8 0 45.3l192 192z"
              />
            </svg>
          </div> -->
          <!-- dropdown -->
          <!-- <div class="absolute top-0 pt-10 left-0 hidden group-hover:block">
            <div
              class="bg-[#fff] rounded-md w-max space-y-3 px-5 py-3 shadow-lg"
            >
              <a href="/schools/product" class="text-base font-medium block"
                >School of Product</a
              >
              <a href="/schools/engineering" class="text-base font-medium block"
                >School of Engineering</a
              >
              <a href="/schools/data" class="text-base font-medium block"
                >School of Data</a
              >
            </div>
          </div> -->
        <!-- </div> -->
        <!-- community  -->
       <a href="/#onboard" class="text-base font-medium">About</a> 
       <button class="text-base font-medium" @click="toggleCommunityPopUp">
          Join Our Community
        </button> 

        

        

        <!-- with dropdown -->
        <div class="relative group cursor-pointer">
          <div class="flex items-center gap-2">
            <p class="text-base font-medium">Support</p>
            <svg
              xmlns="http://www.w3.org/2000/svg"
              viewBox="0 0 512 512"
              width="15"
              height="15"
              class="group-hover:rotate-180 duration-300"
            >
              <path
                d="M233.4 406.6c12.5 12.5 32.8 12.5 45.3 0l192-192c12.5-12.5 12.5-32.8 0-45.3s-32.8-12.5-45.3 0L256 338.7 86.6 169.4c-12.5-12.5-32.8-12.5-45.3 0s-12.5 32.8 0 45.3l192 192z"
              />
            </svg>
          </div>
          <!-- dropdown -->
          <div class="absolute top-0 pt-10 left-0 hidden group-hover:block">
            <div
              class="bg-[#fff] rounded-md w-max space-y-3 px-5 py-3 shadow-lg"
            >
              <a href="/faqs" class="text-base font-medium block">FAQs</a>
              <button
                class="text-base font-medium block"
                @click="toggleContactPopUp"
              >
                Contact Us
              </button>
            </div>
          </div>
        </div>
      </div>

      <!-- cta -->
      <div class="place-items-center hidden md:grid">
        <a href="/application" class="btn-primary">Donate</a>
      </div>

      <!-- hamburger -->
      <div class="cursor-pointer md:hidden" @click="toggleMobile">
        <svg
          xmlns="http://www.w3.org/2000/svg"
          viewBox="0 0 448 512"
          width="20"
          height="15"
        >
          <path
            d="M0 96C0 78.3 14.3 64 32 64H416c17.7 0 32 14.3 32 32s-14.3 32-32 32H32C14.3 128 0 113.7 0 96zM0 256c0-17.7 14.3-32 32-32H416c17.7 0 32 14.3 32 32s-14.3 32-32 32H32c-17.7 0-32-14.3-32-32zM448 416c0 17.7-14.3 32-32 32H32c-17.7 0-32-14.3-32-32s14.3-32 32-32H416c17.7 0 32 14.3 32 32z"
          />
        </svg>
      </div>

      <!-- mobile menu -->
      <div
        v-if="showMobile"
        class="fixed inset-0 h-screen w-full bg-white px-5 md:hidden duration-300"
      >
        <!-- close icon -->
        <div class="absolute right-5 top-5" @click="toggleMobile">
          <svg
            xmlns="http://www.w3.org/2000/svg"
            viewBox="0 0 384 512"
            width="25"
            height="25"
          >
            <path
              d="M342.6 150.6c12.5-12.5 12.5-32.8 0-45.3s-32.8-12.5-45.3 0L192 210.7 86.6 105.4c-12.5-12.5-32.8-12.5-45.3 0s-12.5 32.8 0 45.3L146.7 256 41.4 361.4c-12.5 12.5-12.5 32.8 0 45.3s32.8 12.5 45.3 0L192 301.3 297.4 406.6c12.5 12.5 32.8 12.5 45.3 0s12.5-32.8 0-45.3L237.3 256 342.6 150.6z"
            />
          </svg>
        </div>

        <!-- links -->
        <div class="pt-32 grid grid-cols-2 gap-8">
          <!-- schools -->
          <!-- <div class="space-y-8">
            <header class="uppercase font-bold text-base">schools</header>
            <a href="/schools/product" class="text-sm font-medium block"
              >School of Product</a
            >
            <a href="/schools/data" class="text-sm font-medium block"
              >School of Data</a
            >
            <a href="/schools/engineering" class="text-sm font-medium block"
              >School of Engineering</a
            >
          </div> -->

          <!-- company -->
          <div class="space-y-8">
            <header class="uppercase font-bold text-base">company</header>
            <a href="/#onboard" class="text-sm font-medium block">About</a>
            <a href="/faqs" class="text-sm font-medium block">FAQs</a>
            <button
              class="text-sm font-medium block"
              @click="toggleCommunityPopUp"
            >
              Join The Community
            </button>
            <a href="/partners" class="text-sm font-medium block"
              >Partnership</a
            >
          </div>

          <!-- help -->
          <div class="space-y-8">
            <header class="uppercase font-bold text-base">help</header>
            <a
              href="mailto:codelr@gmail.com"
              class="text-sm font-medium block"
              >codelr@gmail.com</a
            >
            <a href="tel:+2349015558035" class="text-sm font-medium block"
              >09081997316</a
            >
          </div>
        </div>
      </div>
    </nav>
  </header>

  <div v-if="showCommunityPopUp">
    <JoinOurCommunityPopUp :toggleCommunityPopUp="toggleCommunityPopUp" />
  </div>

  <div v-if="showContactPopUp">
    <ContactPopUp :toggleContactPopUp="toggleContactPopUp" />
  </div>
</template>
