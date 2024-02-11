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
    name: "About",
    path: "/about",
  },
  {
    name: "Contact",
    path: "/contact",
  },
];
</script>

<style scoped></style>
