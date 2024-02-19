<template>
  <div>
    <div>
      <div>
        <img class="main_img w-full" src="https://influencedigest.com/wp-content/uploads/2023/01/Best-Skincare-Brands-Locally-made-in-New-York.jpg"  alt=""/>
      </div>
      <div class="container">
      <span class="image_heading">
        Love Your Skin Naturally
      </span>
      </div>
    </div>
  </div>
  <div>
    <ImageSlider />
  </div>
</template>

<script>

import ImageSlider from "@/components/pages/landing/slider/ImageSlider.vue";

export default {
  name: "LandingPage",
  components: {ImageSlider},
}

</script>
<style scoped>
  .main_img{
    height: 800px;
    object-fit: cover;
  }

  .container {
    position: absolute;
    top: 40%;
    left: 35%;
    transform: translate(-70%, -50%);
  }

  .container > span {
    display: block;
    text-align: center;
    text-transform: uppercase;
  }

  .image_heading {
    font-size: 3rem;
    font-weight: 500;
    margin-bottom: 0;
    animation: textBounceStretch 3s 1;
    position: relative;
  }

  @keyframes textBounceStretch {
    0% {
      color: white;
      margin-bottom: -40px;
    }
    30% {
      letter-spacing: 13px;
      margin-bottom: -40px;
    }
    85% {
      letter-spacing: 8px;
      margin-bottom: -40px;
    }
  }
</style>