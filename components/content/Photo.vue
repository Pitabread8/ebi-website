<script setup>
defineProps(["img"]);
</script>

<template>
  <NuxtImg :src="'/blog/' + [img]" class="my-4 rounded-xl" />
</template>
