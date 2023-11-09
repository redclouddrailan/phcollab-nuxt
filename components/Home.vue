<script setup>

</script>

<template>
  <div
    class="bg-fixed bg-cover bg-[url('assets/images/bg.png')] h-screen flex items-center justify-center">
    <div class="max-w-7xl m-auto text-white">
      <!-- main body section -->
      <div class="grid grid-cols-12 gap-6">
        <!-- tag line component -->
        <Tagline />
        <div class="col-span-6">
          <!-- main content -->
          <Hero :title="`Powering Progress with Technology`" :description="`Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.`"/>
        </div>
        <div class="col-span-5 bg-white p-8 rounded-lg">       
          <HubspotForm />
        </div>
      </div>
    </div>
  </div>
</template>
