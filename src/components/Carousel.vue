<template>
    <div class="container">
        <section class="carousel">
            <h2 class="carousel-title">Previously viewed products</h2>

            <div class="carousel-container">

                <button class="Prev">
                    <img src="@/assets/icons/prev-slider.svg">
                </button>
                <button class="Next">
                    <img src="@/assets/icons/next.svg">
                </button>

                <swiper class="mySwiper swiper" style="width: unset;"
                    :navigation="{ nextEl: '.Next', prevEl: '.Prev' }"
                    :slidesPerView="6.6"
                    :spaceBetween="10"
                    :slidesPerGroup="1"
                    :modules="modules"
                    clickable: true
                    @swiper="onSwiper"
                    @slideChange="onSlideChange"
                >
                    <swiper-slide class="swiper-item" style="min-width: 135px; max-width: 187px; margin-right: 0px;"
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
                                    <img src="@/assets/icons/like-slider.svg">
                                </a>
                            </div>
                            <div class="carousel-item__descr">
                                <span class="carousel-item__descr--price">{{ product.price }} $ <span>{{ product.oldprice }} $</span></span>
                                <p class="carousel-item__descr--text">{{ product.name }}</p>
                                <a href="#" class="carousel-item__descr--link">{{ product.link }}</a>
                            </div>
                            <div class="carousel-item__raiting">
                                <div class="carousel-item__raiting--items">
                                    <img src="@/assets/icons/star-active-desk.svg">
                                    <img src="@/assets/icons/star-active-desk.svg">
                                    <img src="@/assets/icons/star-active-desk.svg">
                                    <img src="@/assets/icons/star-active-desk.svg">
                                    <img src="@/assets/icons/star-desk.svg">
                                </div>
                                <p class="carousel-item__raiting--reviews">25 reviews</p>
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
import SwiperCore, { Pagination, Navigation } from 'swiper'
import { Swiper, SwiperSlide } from 'swiper/vue'
import "swiper/swiper.scss";

import "swiper/components/pagination/pagination.scss";
import "swiper/components/navigation/navigation.scss";

SwiperCore.use([Navigation, Pagination])

  export default {
    components: {
      Swiper,
      SwiperSlide
    },
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
    //   const onSwiper = (swiper) => {
    //     console.log(swiper);
    //   };
    //   const onSlideChange = () => {
    //     console.log('slide change');
    //   };
      return {
        // onSwiper,
        // onSlideChange,
        modules: [Pagination, Navigation]
     };
    },
  };
</script>