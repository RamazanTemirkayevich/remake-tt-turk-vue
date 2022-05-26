<template>
    <div class="container">
        <section class="review">
            <div class="review-box">
                <div class="review-box__container">
                    <div class="review-box__container--raiting">
                        <div class="raiting-stars">
                            <img src="@/assets/icons/star-active2.svg" alt="">
                            <img src="@/assets/icons/star-active2.svg" alt="">
                            <img src="@/assets/icons/star-active2.svg" alt="">
                            <img src="@/assets/icons/star-active2.svg" alt="">
                            <img src="@/assets/icons/star2.svg" alt="">
                        </div>
                        <span class="raiting-grade">4.5 / 5</span>
                    </div>

                    <hr class="line">

                    <div class="review-box__container--bar">
                        <div class="bar-item">
                            <p>5 stars</p>
                            <div class="bar-item__line">
                                <div class="progresive"></div>
                            </div>
                            <span>15</span>
                        </div>
                        <div class="bar-item">
                            <p>4 stars</p>
                            <div class="bar-item__line">
                                <div class="progresive-second"></div>
                            </div>
                            <span>4</span>
                        </div>
                        <div class="bar-item">
                            <p>3 stars</p>
                            <div class="bar-item__line">
                                <div class="progresive-third"></div>
                            </div>
                            <span>5</span>
                        </div>
                        <div class="bar-item">
                            <p>2 stars</p>
                            <div class="bar-item__line">
                                <div class="progresive-fourth"></div>
                            </div>
                            <span>2</span>
                        </div>
                        <div class="bar-item">
                            <p>1 star</p>
                            <div class="bar-item__line">
                                <div class="progresive-fifth"></div>
                            </div>
                            <span>0</span>
                        </div>
                    </div>

                    <a class="review-box__container--btn">Write a review</a>
                </div>
            </div>

            <h2 class="review-title">Reviews and ratings<span>(25)</span></h2>

            <select name="" id="">
                <option value="">Helpful first</option>
                <option value=""></option>
                <option value=""></option>
            </select>

            <div class="review-images">
                <p class="review-images__title">Buyer Photos</p>
                
                <div class="review-images__items">
                    <swiper class="review-swiper"
                        :slides-per-view="2.5"
                        :space-between="30"
                        @swiper="onSwiper"
                        @slideChange="onSlideChange"
                    >
                        <swiper-slide class="review-swiper__slide">
                            <Review-images
                                v-for="img in images"
                                v-bind:key="img.item"
                                :img_data="img"
                            />
                        </swiper-slide>

                    </swiper>
                </div>
            </div>

            <div class="review-comments">
                <div class="review-comments__first"></div>
                <div class="review-comments__second"></div>
            </div>
        </section>
    </div>
</template>

<script>
import { Swiper, SwiperSlide } from 'swiper/vue';
import ReviewImages from './Review-images.vue'

export default {
    components: {
        Swiper,
        SwiperSlide,
        ReviewImages
    },
    data() {
        return {
            images: [
                {
                    item: "image44.png"
                },
                {
                    item: "image48.png"
                },
                {
                    item: "image49.png"
                },
                {
                    item: "image50.png"
                },
                {
                    item: "image44.png"
                },
                {
                    item: "image48.png"
                }
            ]
        }
    }
}
</script>