<template>
  <header>
    <div class="header-content flex gap-5 justify-content-center align-items-center w-full fixed p-2">
      <p class="text-sm font-medium">HOME</p>
      <p class="text-sm font-medium">SHOP</p>
      <div class="flex flex-column align-items-center">
        <img class="w-4rem" src="../../../../public/beauty_logo.png" alt=""/>
      </div>
      <p class="text-sm font-medium">ABOUT US</p>
      <p class="text-sm font-medium">CONTACT US</p>
    </div>
  </header>
</template>

<script>
export default {
  name: "HeaderPart"
}
</script>

<style scoped>
.header-content{
  backdrop-filter: blur(10px);
}
</style>