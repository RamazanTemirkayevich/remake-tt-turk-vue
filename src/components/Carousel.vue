<template>
    <div class="container">
        <section class="carousel">
            <h2 class="carousel-title">Previously viewed products</h2>

            <div class="carousel-container">

                <!-- <button @click="MovePrev" class="prev"></button>
                <button @click="MoveNext" class="next"></button> -->

                <swiper class="swiper"
                    :navigation="true"
                    :modules="modules"
                    :slides-per-view="2.5"
                    :space-between="50"
                    @swiper="onSwiper"
                    @slideChange="onSlideChange"
                >
                    <swiper-slide style="min-width: 135px; max-width: 187px; margin-left: 15px; margin-right: unset;"
                        v-for="product in products"
                        :key="product.id"
                    >
                        <div class="carousel-item">
                            <div class="carousel-item__img">
                                <img :src=" require('../assets/slide_img/' + product.image)" alt="">
                                <div class="carousel-item__img--sale">
                                    <span>{{ product.sale }}</span>
                                </div>
                                <a class="carousel-item__img--favorite">
                                    <img src="@/assets/icons/like.svg">
                                </a>
                            </div>
                            <div class="carousel-item__descr">
                                <span class="carousel-item__descr--price">{{ product.price }} $ <span>{{ product.oldprice }} $</span></span>
                                <p class="carousel-item__descr--text">{{ product.name }}</p>
                                <a href="#" class="carousel-item__descr--link">{{ product.link }}</a>
                            </div>
                        </div>

                        <div class="carousel-item-desktop">

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

  export default {
    components: {
      Swiper,
      SwiperSlide
    },
    methods: {

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
                    link: "Best jeans store",
                    sale: "-12%"
                },
                {
                    id: 2,
                    image: "image33.png",
                    price: 910.15,
                    oldprice: 890.89,
                    name: "Samsung Galaxy S10 8 / 128GB Aquamarine...",
                    link: "Best jeans store",
                    sale: "-15%"
                },
                {
                    id: 3,
                    image: "image31.png",
                    price: 820.15,
                    oldprice: 646.99,
                    name: "Smartphone Apple iPhone 11 64GB, Black",
                    link: "Best jeans store",
                    sale: "-10%"
                },
                {
                    id: 4,
                    image: "image34.png",
                    price: 410.15,
                    oldprice: 546.99,
                    name: "TV box Xiaomi Mi Box S",
                    link: "Best jeans store",
                    sale: "-20%"
                },
                {
                    id: 5,
                    image: "image33.png",
                    price: 910.15,
                    oldprice: 890.89,
                    name: "Samsung Galaxy S10 8 / 128GB Aquamarine...",
                    link: "Best jeans store",
                    sale: "-15%"
                },
                {
                    id: 6,
                    image: "image36.png",
                    price: 810.15,
                    oldprice: 846.99,
                    name: "Smartphone Apple iPhone 11 64GB, red",
                    link: "Best jeans store",
                    sale: "-12%"
                },
                {
                    id: 7,
                    image: "image31.png",
                    price: 810.15,
                    oldprice: 846.99,
                    name: "Smartphone Apple iPhone 11 64GB, red",
                    link: "Best jeans store",
                    sale: "-10%"
                },
                {
                    id: 8,
                    image: "image33.png",
                    price: 810.15,
                    oldprice: 846.99,
                    name: "Smartphone Apple iPhone 11 64GB, red",
                    link: "Best jeans store",
                    sale: "-15%"
                },
                {
                    id: 9,
                    image: "image34.png",
                    price: 810.15,
                    oldprice: 846.99,
                    name: "Smartphone Apple iPhone 11 64GB, red",
                    link: "Best jeans store",
                    sale: "-20%"
                },
                {
                    id: 10,
                    image: "image36.png",
                    price: 810.15,
                    oldprice: 846.99,
                    name: "Smartphone Apple iPhone 11 64GB, red",
                    link: "Best jeans store",
                    sale: "-12%"
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
        onSlideChange
     };
    },
  };
</script>