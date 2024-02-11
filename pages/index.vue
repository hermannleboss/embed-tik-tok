<template>
  <div>
    <nuxt-link v-for="page in pages" :to="page.path" style="display: block"
      ><h2>{{ page.name }}</h2></nuxt-link
    >
  </div>
</template>

<script setup lang="ts">
const pages = [
  {
    name: "Home",
    path: "/",
  },
  {
    name: "1- Iframe",
    path: "/1-iframe",
  },
  {
    name: "2- API",
    path: "/2-api",
  },
];
</script>

<style scoped></style>
