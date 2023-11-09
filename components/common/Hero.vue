<template>
 <!-- logo component -->
    <div class="w-60 grid justify-center items-center grid-cols-3 gap-3">
      <div class="col-span-1">
        <Image :src="logo" />
      </div>
      <div class="col-span-2">
        <Image :src="logoText" alt="" />
      </div>
    </div>
  <div class="">
    <div class="text-7xl mt-20">{{ props.title }}</div>
      <p class="text-lg mt-20">{{ props.description }}</p>
  </div>
</template>

<script setup>
  import logo from "/assets/images/logo.png";
  import logoText from "/assets/images/logo-text.png";
  const props = defineProps(["title", "description"]);
</script>