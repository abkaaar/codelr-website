<script setup>
import SocialComponent from "./SocialComponent.vue"
</script>

<template>
  <div class="container px-5 lg:px-[9.375rem]">
    <div
      class="grid grid-cols-2 md:grid-cols-3 lg:grid-cols-12 gap-8 gap-y-20 md:gap-10 mt-11 md:mt-0 w-full"
    >
      <div
        class="flex flex-col col-span-2 md:col-span-3 lg:col-span-5 space-y-4"
      >
        <img src="/codelrlogo.png" alt="codelr africa" class="w-24 block" />
        <p class="text-lighestgrey md:max-w-[22rem]">
          An organization that is focused on equipping African youths with the
          knowledge and skills needed in the tech space.
        </p>
        <!-- socials -->
        <SocialComponent />
      </div>
      <div class="flex flex-col lg:col-span-3 gap-8 md:order-2">
        <header class="font-bold md:text-lg">SCHOOLS</header>
        <a
          href="/schools/product"
          class="text-lighestgrey text-sm lg:text-base font-medium"
          >School of Product</a
        >
        <a
          href="/schools/data"
          class="text-lighestgrey text-sm lg:text-base font-medium"
          >School of Data</a
        >
        <a
          href="/schools/engineering"
          class="text-lighestgrey text-sm lg:text-base font-medium"
          >School of Engineering</a
        >
      </div>
      <div class="flex flex-col lg:col-span-2 gap-8 md:order-1">
        <header class="font-bold md:text-lg">COMPANY</header>
        <a
          href="/#onboard"
          class="text-lighestgrey text-sm lg:text-base font-medium"
          >About</a
        >
        <a href="/#" class="text-lighestgrey text-sm lg:text-base font-medium"
          >Blog</a
        >
        <a
          href="/faqs"
          class="text-lighestgrey text-sm lg:text-base font-medium"
          >FAQs</a
        >
        <a
          href="/application"
          class="text-lighestgrey text-sm lg:text-base font-medium"
          >Join Our Community</a
        >
        <a
          href="/partners"
          class="text-lighestgrey text-sm lg:text-base font-medium"
          >Partnership</a
        >
      </div>
      <div class="flex flex-col lg:col-span-1 gap-8 md:order-3">
        <header class="font-bold md:text-lg text-base">CONTACT</header>
        <a href="mailto:codelr@gmail.com" class="text-sm font-medium block"
          >codelr@gmail.com</a
        >
        <a href="tel:+2349015558035" class="text-sm font-medium block"
          >09081997316</a
        >
      </div>
      <div class="md:hidden">
        <SocialComponent />
      </div>
    </div>

    <p class="w-full text-center mt-16 md:mt-32">
      © 2024 codelr. All rights reserved.
    </p>
  </div>
</template>
