<template>
    <section class="promo">
        <div class="promo-img">
            <swiper
                :navigation="true"
                :modules="modules"
                class="mySwipe swiperr"
            >
                <swiper-slide class="swiper-slide" v-for="items in images" :key="items.id">
                    <img :src="items.item">
                </swiper-slide>
            </swiper>
            <div class="promo-img__index">
                <span>1</span>/<span>4</span>
            </div>
        </div>
        <div class="promo-back">
            <a href="#">
                <img src="@/assets/icons/back.svg" alt="">
            </a>
        </div>
        <div class="promo-like">
            <a href="#">
                <img src="@/assets/icons/like.svg" alt="">
            </a>
        </div>

        <div class="container">
            <div class="promo-container">
                <div class="promo-img__desktop">
                    <div class="promo-img__desktop--column">
                        <div class="column-img">
                            <img src="@/assets/column_img/image44.png" alt="column img">
                        </div>
                        <div class="column-img">
                            <img src="@/assets/column_img/image48.png" alt="column img">
                        </div>
                        <div class="column-img">
                            <img src="@/assets/column_img/image49.png" alt="column img">
                        </div>
                        <div class="column-img">
                            <img src="@/assets/column_img/image50.png" alt="column img">
                        </div>
                        <div class="column-img">
                            <img src="@/assets/column_img/image44.png" alt="column img">
                        </div>
                        <div class="column-img">
                            <img src="@/assets/column_img/image48.png" alt="column img">
                        </div>
                    </div>

                    <div class="promo-img__desktop--main">
                        <img src="@/assets/image44.png" alt="promo image">
                    </div>
                </div>

                <div class="promo-descr">
                    <div class="promo-descr__retail">
                        <p class="promo-descr__retail--text">Retail price</p>
                        <span class="price">14,25 $</span> <span class="old-price">15,35 $</span>
                    </div>
                    <div class="promo-descr__wholesale">
                        <p class="promo-descr__wholesale--text">Wholesale price</p>
                        <span class="price">12,50 $</span>
                    </div>
                    <a class="promo-descr__btn">
                        Buy now
                    </a>
                </div>

                <div class="promo-descr-desktop">
                    <div class="promo-color"
                        v-for="color in colors" :key="color.id"
                    >
                        <p class="promo-color__name">Color: <span>{{ color.item }}</span></p>
                        <div class="promo-color__images">
                            <div class="promo-color__images--item">
                                <img src="@/assets/color-img.png" alt="color">
                            </div>
                            <div class="promo-color__images--item">
                                <img src="@/assets/color-img2.png" alt="color">
                            </div>
                        </div>
                    </div>
                    <div class="promo-size">
                        <p class="promo-size__name">
                            Size: <span></span>
                        </p>
                        <div class="promo-size__items">
                            <div class="promo-size__items--index">xs</div>
                            <div class="promo-size__items--index">s</div>
                            <div class="promo-size__items--index">m</div>
                            <div class="promo-size__items--index">l</div>
                            <div class="promo-size__items--index">xl</div>
                            <div class="promo-size__items--index">xxl</div>
                            <div class="promo-size__items--index">xxxl</div>
                        </div>
                    </div>
                    <div class="promo-counter">
                        <p class="promo-counter__title">Amount: <span></span></p>
                        <div class="promo-counter__elements">
                            <div class="counter">
                                <button class="minus">-</button>
                                <span>100</span>
                                <button class="plus">+</button>
                            </div>
                            <p class="amount">12451 pcs. in stock</p>
                        </div>
                    </div>
                </div>
                
                <hr class="promo-line">

                <div class="promo-name">
                    <div class="promo-name__items">
                        <h2 class="promo-name__items--title">Signature gray oversized faux fur shirt</h2>
                        <div class="promo-name__items--img">
                            <img src="@/assets/brand.png" alt="">
                        </div>
                    </div>

                    <div class="promo-name__descr">
                        <div class="promo-name__descr--raiting">
                            <div class="raiting-stars">
                                <img src="@/assets/icons/star-active.svg" alt="">
                                <img src="@/assets/icons/star-active.svg" alt="">
                                <img src="@/assets/icons/star-active.svg" alt="">
                                <img src="@/assets/icons/star-active.svg" alt="">
                                <img src="@/assets/icons/star.svg" alt="">
                            </div>
                            <span class="raiting-text">485 reviews</span>
                        </div>
                        <p class="promo-name__descr--code">Product code: <span>2138815</span></p>
                        <p class="promo-name__descr--text">Bought more than 512882 times</p>
                    </div>
                </div>

                <hr class="promo-line">

                <div class="promo-information">
                    <p class="promo-infromation__price">Delivery: <span>5,25 $</span></p>
                    <p class="promo-infromation__time">Estimated delivery time: <span>25/08</span></p>
                    <p class="promo-infromation__brand">
                        Seller: 
                        <span>New Look</span>
                        <img src="@/assets/icons/info.svg" alt="">
                    </p>
                </div>

                <hr class="promo-line">
            </div>
        </div>
    </section>
</template>

<script>
import { Swiper, SwiperSlide } from "swiper/vue"

import { Pagination, Navigation } from "swiper"
export default {
    components: {
        Swiper,
        SwiperSlide
    },
    setup() {
        return {
        modules: [Pagination, Navigation],
        };
    },
    data() {
        return {
            images: [
                {   
                    id: 1,
                    item: require("../assets/image44.png")
                },
                {
                    id: 2,
                    item: require("../assets/column_img/image48.png")
                },
                {
                    id: 3,
                    item: require("../assets/column_img/image49.png")
                },
                {
                    id: 4,
                    item: require("../assets/column_img/image50.png")
                }
            ],
            colors: [
                {
                    id: 1,
                    item: "Blue"
                }
            ]
        }
    }
}
</script>