<template>
  <HeaderPart />
  <LandingPage />
</template>

<script>
import LandingPage from "@/components/pages/landing/LandingPage.vue";
import HeaderPart from "@/components/pages/header/Header.vue";

export default {
  name: 'App',
  components: {
    HeaderPart,
    LandingPage
  }
}
</script>

<style>
*{
  margin: 0;
}
</style>