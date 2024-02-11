<template>
  <div>
    <!-- Back to home link -->
    <nuxt-link to="/" style="font-size: 25px;">Back to home</nuxt-link>
    <NuxtPage>  
      
    </NuxtPage>
  </div>
</template>
<script lang="ts" setup>
useHead({
  script: [
    {
      async: true,
      src: 'https://www.tiktok.com/embed.js'
    }
  ]
})</script>

<style>
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}
</style>
