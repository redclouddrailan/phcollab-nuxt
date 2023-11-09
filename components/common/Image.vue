<script setup>
const props = defineProps(["src"]);
</script>

<template>
  <img :src="props.src" class="object-contain w-full" />
</template>
