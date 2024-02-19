<template>
  <div class="card">
    <Carousel :value="products" :numVisible="3" :numScroll="1" :responsiveOptions="responsiveOptions" circular :autoplayInterval="3000">
      <template #item="slotProps">
        <div class="w-full border-1 surface-border border-round m-2  p-3">
          <div class="mb-3">
            <div class="relative mx-auto">
              <img :src="slotProps.data.image" :alt="slotProps.data.name" class="slider-img w-full border-round" />
              <Tag :value="slotProps.data.inventoryStatus" :severity="getSeverity(slotProps.data.inventoryStatus)" class="absolute" style="left:5px; top: 5px"/>
            </div>
          </div>
          <div class="mb-3 font-medium">{{ slotProps.data.name }}</div>
          <div class="flex justify-content-between align-items-center">
            <div class="mt-0 font-semibold text-xl">${{ slotProps.data.price }}</div>
          </div>
        </div>
      </template>
    </Carousel>
  </div>
</template>

<script>
import { ProductService } from './service/ProductService';
import Carousel from "primevue/carousel";

export default {
  components:{
    Carousel
  },
  data() {
    return {
      products: null,
      responsiveOptions: [
        {
          breakpoint: '1400px',
          numVisible: 2,
          numScroll: 1
        },
        {
          breakpoint: '1199px',
          numVisible: 3,
          numScroll: 1
        },
        {
          breakpoint: '767px',
          numVisible: 2,
          numScroll: 1
        },
        {
          breakpoint: '575px',
          numVisible: 1,
          numScroll: 1
        }
      ]
    };
  },
  mounted() {
    ProductService.getProductsSmall().then((data) => (this.products = data.slice(0, 9)));
  },
  methods: {
    getSeverity(status) {
      switch (status) {
        case 'INSTOCK':
          return 'success';

        case 'LOWSTOCK':
          return 'warning';

        case 'OUTOFSTOCK':
          return 'danger';

        default:
          return null;
      }
    }
  }
};
</script>

<style scoped>
.slider-img{
  object-fit: cover;
  height: 450px;
}

>>> .p-carousel-items-container{
  gap: 30px;
}
</style>
