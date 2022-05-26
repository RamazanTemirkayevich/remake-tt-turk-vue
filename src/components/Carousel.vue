<template>
    <div class="container">
        <section class="carousel">
            <h2 class="carousel-title">Previously viewed products</h2>

            <div class="carousel-container">
                <swiper class="swiper"
                    :slides-per-view="2.5"
                    :space-between="50"
                    @swiper="onSwiper"
                    @slideChange="onSlideChange"
                >
                    <swiper-slide class="swiper-slide">
                        <CarouselItem
                            v-for="product in products"
                            v-bind:key="product.price"
                            :product_data="product"
                        />
                    </swiper-slide>
                    ...
                </swiper>
            </div>

            <hr class="carousel-line">
        </section>
    </div>
</template>

<script>
import { Swiper, SwiperSlide } from 'swiper/vue';
import CarouselItem from './CarouselItem.vue'

  export default {
    components: {
      Swiper,
      SwiperSlide,
      CarouselItem
    },
    props: {},
    data() {
        return {
            products: [
                {
                    image: "image36.png",
                    price: 810.15,
                    oldprice: 846.99,
                    name: "Smartphone Apple iPhone 11 64GB, red",
                    link: "Best jeans store"
                },
                {
                    image: "image33.png",
                    price: 910.15,
                    oldprice: 890.89,
                    name: "Samsung Galaxy S10 8 / 128GB Aquamarine...",
                    link: "Best jeans store"
                },
                {
                    image: "image31.png",
                    price: 820.15,
                    oldprice: 646.99,
                    name: "Smartphone Apple iPhone 11 64GB, black",
                    link: "Best jeans store"
                },
                {
                    image: "image34.png",
                    price: 410.15,
                    oldprice: 546.99,
                    name: "TV box Xiaomi Mi Box S",
                    link: "Best jeans store"
                },
                {
                    image: "image33.png",
                    price: 910.15,
                    oldprice: 890.89,
                    name: "Samsung Galaxy S10 8 / 128GB Aquamarine...",
                    link: "Best jeans store"
                },
                {
                    image: "image36.png",
                    price: 810.15,
                    oldprice: 846.99,
                    name: "Smartphone Apple iPhone 11 64GB, red",
                    link: "Best jeans store"
                }
            ]
        }
    },
    setup() {
      const onSwiper = (swiper) => {
        console.log(swiper);
      };
      const onSlideChange = () => {
        console.log('slide change');
      };
      return {
        onSwiper,
        onSlideChange,
      };
    },
  };
</script>