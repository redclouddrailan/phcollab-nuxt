<script setup>
import logo from "/assets/images/logo.png";
import logoText from "/assets/images/logo-text.png";
</script>

<template>
  <div
    class="bg-fixed bg-cover bg-[url('assets/images/bg.png')] h-screen flex items-center justify-center"
  >
    <div class="max-w-7xl m-auto text-white">
      <!-- main body section -->
      <div class="grid grid-cols-12 gap-6">
        <div
          class="[writing-mode:vertical-rl] rotate-180 col-span-1 flex justify-center h-100"
        >
          <div class="mb-16">Code</div>
          <div class="mb-16">Collaborate</div>
          <div class="mb-16">Create</div>
        </div>
        <div class="col-span-6">
          <!-- logo component -->
          <div class="w-60 grid justify-center items-center grid-cols-3 gap-3">
            <div class="col-span-1">
              <Image :src="logo" />
            </div>
            <div class="col-span-2">
              <Image :src="logoText" alt="" />
            </div>
          </div>

          <!-- main content -->
          <div class="">
            <div class="text-7xl mt-20">Powering Progress with Technology</div>
            <p class="text-lg mt-20">
              A software development company located at Sorsogon City,
              Philippines.
            </p>
          </div>
        </div>
        <div class="col-span-5 bg-white p-8 rounded-lg">
          <p class="text-purple-950 text-center font-bold text-3xl mb-8">
            Speak with Us!
          </p>
          <HubspotForm />
        </div>
      </div>
    </div>
  </div>
</template>
