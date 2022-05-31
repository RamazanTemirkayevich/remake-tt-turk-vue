<template>
    <div class="container">
        <section class="carousel">
            <h2 class="carousel-title">Previously viewed products</h2>

            <div class="carousel-container">
                <swiper class="swiper"
                    :scrollbar="{
                    hide: true,
                    }"
                    :modules="modules"
                    :slides-per-view="2.5"
                    :space-between="50"
                    @swiper="onSwiper"
                    @slideChange="onSlideChange"
                >
                    <swiper-slide style="width: 135px; margin-right: 0px;"
                        v-for="product in products"
                        :key="product.id"
                    >
                        <div class="carousel-item">
                            <div class="carousel-item__img">
                                <img :src=" require('../assets/slide_img/' + product.image)" alt="">
                            </div>
                            <div class="carousel-item__descr">
                                <span class="carousel-item__descr--price">{{ product.price }} $ <span>{{ product.oldprice }} $</span></span>
                                <p class="carousel-item__descr--text">{{ product.name }}</p>
                                <a href="#" class="carousel-item__descr--link">{{ product.link }}</a>
                            </div>
                        </div>
                    </swiper-slide>
                    ...
                </swiper>
            </div>

            <hr class="carousel-line">
        </section>
    </div>
</template>

<script>
import { Swiper, SwiperSlide } from 'swiper/vue'
import { Scrollbar } from "swiper"

  export default {
    components: {
      Swiper,
      SwiperSlide
    },
    props: {},
    data() {
        return {
            products: [
                {
                    id: 1,
                    image: "image36.png",
                    price: 810.15,
                    oldprice: 846.99,
                    name: "Smartphone Apple iPhone 11 64GB, Red",
                    link: "Best jeans store"
                },
                {
                    id: 2,
                    image: "image33.png",
                    price: 910.15,
                    oldprice: 890.89,
                    name: "Samsung Galaxy S10 8 / 128GB Aquamarine...",
                    link: "Best jeans store"
                },
                {
                    id: 3,
                    image: "image31.png",
                    price: 820.15,
                    oldprice: 646.99,
                    name: "Smartphone Apple iPhone 11 64GB, Black",
                    link: "Best jeans store"
                },
                {
                    id: 4,
                    image: "image34.png",
                    price: 410.15,
                    oldprice: 546.99,
                    name: "TV box Xiaomi Mi Box S",
                    link: "Best jeans store"
                },
                {
                    id: 5,
                    image: "image33.png",
                    price: 910.15,
                    oldprice: 890.89,
                    name: "Samsung Galaxy S10 8 / 128GB Aquamarine...",
                    link: "Best jeans store"
                },
                {
                    id: 6,
                    image: "image36.png",
                    price: 810.15,
                    oldprice: 846.99,
                    name: "Smartphone Apple iPhone 11 64GB, red",
                    link: "Best jeans store"
                },
                {
                    id: 7,
                    image: "image31.png",
                    price: 810.15,
                    oldprice: 846.99,
                    name: "Smartphone Apple iPhone 11 64GB, red",
                    link: "Best jeans store"
                },
                {
                    id: 8,
                    image: "image33.png",
                    price: 810.15,
                    oldprice: 846.99,
                    name: "Smartphone Apple iPhone 11 64GB, red",
                    link: "Best jeans store"
                },
                {
                    id: 9,
                    image: "image34.png",
                    price: 810.15,
                    oldprice: 846.99,
                    name: "Smartphone Apple iPhone 11 64GB, red",
                    link: "Best jeans store"
                },
                {
                    id: 10,
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
        modules: [Scrollbar],
      };
    },
  };
</script>