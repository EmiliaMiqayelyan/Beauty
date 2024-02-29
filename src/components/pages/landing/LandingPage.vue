<template>
  <div>
    <div>
      <div>
        <img class="main_img w-full"
             src="https://influencedigest.com/wp-content/uploads/2023/01/Best-Skincare-Brands-Locally-made-in-New-York.jpg"
             alt=""/>
      </div>
      <div class="container">
      <span class="image_heading">
        Love Your Skin Naturally
      </span>
      </div>
    </div>
  </div>
  <div class="p-6">
    <div>
      <p class="text-center text-5xl font-medium my-4 mt-8 pt-5">Feature Products</p>
    </div>
    <ImageSlider/>
  </div>

  <div class="flex justify-content-around p-6">
    <div class="mt-8 pt-8">
      <p class="w-5 text-5xl font-medium my-4">BEAUTY INSPIRED BY REAL LIFE</p>
      <p class="w-5 text-base line-height-3" style="color: #837E7E">Lorem ipsum dolor sit amet, consectetur adipisicing
        elit. Ab adipisci aperiam architecto consequuntur dignissimos
        doloremque eaque hic in incidunt ipsa.
      </p>
      <div class="mt-6">
        <a class="underline	font-medium text-xl">Discover Now <i class="pi pi-arrow-right text-xs"></i></a>
      </div>
    </div>

    <div class="relative">
      <div id="container">
        <div id="circle">
          <svg version="1.1" xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" x="0px" y="0px"
               width="300px" height="300px" viewBox="0 0 300 300" enable-background="new 0 0 300 300"
               xml:space="preserve">
            <defs>
                <path id="circlePath" d="M 150, 150 m -60, 0 a 60,60 0 0,1 120,0 a 60,60 0 0,1 -120,0 "/>
            </defs>
            <circle cx="150" cy="100" r="75" fill="none"/>
            <g>
            <use xlink:href="#circlePath" fill="none"/>
              <text fill="#000">
                <textPath xlink:href="#circlePath">GET THE GLOW BE YOUR KIND OF BEAUTY</textPath>
              </text>
          </g>
        </svg>
        </div>
      </div>
      <img class="small_img" src="https://thehealinghappymethod.com/cdn/shop/files/SkinCareKitsquare.png?v=1693588751" alt=""/>
      <img src="https://thenaturalskinstore.com/cdn/shop/products/Luxewithbottles_boxes_600x.jpg?v=1664492204" alt=""/>
    </div>
  </div>

  <div class="p-6 flex gap-8">
    <div>
      <img class="timer-img" src="https://cdn05.zipify.com/VNGisZeIVCvJ2K24mzpFklixtRg=/0x0:1755x1755/fit-in/1080x0/5b4253dd04804721b182aca95085f70e/untitled-design-60.png" alt=""/>
    </div>

    <div>
      <p>Save on Sets</p>
      <p>Mode using clean non-toxic ingredients, out products are designed for everyone.</p>
    </div>
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
.main_img {
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

.small_img{
  width: 250px;
  height: 280px;
  object-fit: cover;
  position: absolute;
  left: -30%;
  top: 50%;
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

#container { margin: 0; }

#circle { position: relative; width: 100%; padding-bottom: 10%;}

#circle text { font-family: 'Helvetica Neue', Arial; font-size: 16px; font-weight: bold; }

#circle svg { position: absolute; width: 100%;
  left: -80%;
  top: 300%;
  z-index: 4;
  -webkit-animation-name: rotate;
  -moz-animation-name: rotate;
  -ms-animation-name: rotate;
  -o-animation-name: rotate;
  animation-name: rotate;
  -webkit-animation-duration: 5s;
  -moz-animation-duration: 5s;
  -ms-animation-duration: 5s;
  -o-animation-duration: 5s;
  animation-duration: 5s;
  -webkit-animation-iteration-count: infinite;
  -moz-animation-iteration-count: infinite;
  -ms-animation-iteration-count: infinite;
  -o-animation-iteration-count: infinite;
  animation-iteration-count: infinite;
  -webkit-animation-timing-function: linear;
  -moz-animation-timing-function: linear;
  -ms-animation-timing-function: linear;
  -o-animation-timing-function: linear;
  animation-timing-function: linear;

}

@-webkit-keyframes rotate {
  from { -webkit-transform: rotate(360deg); }
  to { -webkit-transform: rotate(0); }
}
@-moz-keyframes rotate {
  from { -moz-transform: rotate(360deg); }
  to { -moz-transform: rotate(0); }
}
@-ms-keyframes rotate {
  from { -ms-transform: rotate(360deg); }
  to { -ms-transform: rotate(0); }
}
@-o-keyframes rotate {
  from { -o-transform: rotate(360deg); }
  to { -o-transform: rotate(0); }
}
@keyframes rotate {
  from { transform: rotate(360deg); }
  to { transform: rotate(0); }
}

.timer-img{
  width: 700px;
  height: 700px;
  object-fit: cover;
}
</style>