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

                    <a @click="() => ToggleModal('buttonTrigger')" class="review-box__container--btn">Write a review</a>
                </div>
            </div>

            <div class="review-comments__block">
                <div class="review-title-box">
                    <h2 class="review-title">Reviews and ratings<span>(25)</span></h2>
                    
                    <div class="review-select">
                        <select name="" id="">
                            <option value="">Helpful first</option>
                            <option value=""></option>
                            <option value=""></option>
                        </select>
                    </div>
                </div>

                <hr class="review-comments__line">

                <div class="review-images">
                    <p class="review-images__title">Buyer Photos</p>

                    <button class="prev">
                        <img src="@/assets/icons/prev-slider.svg">
                    </button>
                    <button class="next">
                        <img src="@/assets/icons/next.svg">
                    </button>
                    
                    <div class="review-images__items">
                        <swiper class="review-swiper"
                            :navigation="{ nextEl: '.next', prevEl: '.prev' }"
                            :slidesPerView="5.5"
                            :spaceBetween="10"
                            :slidesPerGroup="1"
                            :modules="modules"
                            @swiper="onSwiper"
                            @slideChange="onSlideChange"
                        >
                            <swiper-slide v-for="img in images" :key="img.id" class="review-swiper__slide" style="max-width: 148px; min-width: 79px; max-heigth: 187px; min-heigth: 100px; margin-right: 0px;">
                                <div class="images">
                                    <img :src="img.item" alt="">
                                </div>
                            </swiper-slide>

                        </swiper>
                    </div>
                </div>

                <hr class="review-comments__line--02">

                <div class="review-comments">
                    <div class="review-comments__user">
                        <Users/>                    
                    </div>
                </div>
            </div>

            <Modal class="modal"
                v-if="ModalTriggers.buttonTrigger"
                :ToggleModal="() => ToggleModal('buttonTrigger')"
                >
                <div class="modal-box">
                    <div class="modal-box__container">
                        <form action="">
                            <div class="modal-box__container--title">
                                <label class="modal-name">Write a review</label>
                                <button class="modal-close" @click="() => ToggleModal('buttonTrigger')">
                                    <img src="@/assets/icons/close.svg">
                                </button>
                            </div>
                            <div class="modal-box__container--raiting">
                                <p class="raiting-title">How would you rate the product?</p>
                                <div class="raiting-stars">
                                    <img src="@/assets/icons/star-active.svg">
                                    <img src="@/assets/icons/star-active.svg">
                                    <img src="@/assets/icons/star-active.svg">
                                    <img src="@/assets/icons/star.svg">
                                    <img src="@/assets/icons/star.svg">
                                </div>
                            </div>
                            <div class="advantages-form">
                                <p class="advantages-form__title">Advantages</p>
                                <input type="text" placeholder="Product advantages">
                            </div>
                            <div class="disadvantages-form">
                                <p class="disadvantages-form__title">Disadvantages</p>
                                <input type="text" placeholder="Product disadvantages">
                            </div>
                            <div class="comment-form">
                                <p class="comment-form__title">Comment</p>
                                <textarea class="comment-form__input" rows="4" cols="47" placeholder="Comment about product"></textarea>
                            </div>
                            <div class="upload-images">
                                <p class="upload-images__title">Upload product photos</p>
                                <button class="upload-images__btn">
                                    <img src="@/assets/icons/plus.svg">
                                </button>
                            </div>
                            <a href="#" class="modal-btn">Send a review</a>
                        </form>
                    </div>
                </div>
            </Modal>

        </section>
    </div>
</template>

<script>
import Users from './Users.vue'

import { ref } from 'vue';
import Modal from './Modal.vue'
import SwiperCore, { Pagination, Navigation } from 'swiper'
import { Swiper, SwiperSlide } from 'swiper/vue'
import "swiper/swiper.scss";

import "swiper/components/pagination/pagination.scss";
import "swiper/components/navigation/navigation.scss";

SwiperCore.use([Navigation, Pagination])
export default {
    components: {
        Swiper,
        SwiperSlide,
        Users 
    },
    data() {
        return {
            images: [
                {
                    id: 1,
                    item: require("../assets/column_img/image44.png")
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
                },
                {
                    id: 5,
                    item: require("../assets/column_img/image44.png")
                },
                {
                    id: 6,
                    item: require("../assets/column_img/image48.png")
                },
                {
                    id: 7,
                    item: require("../assets/column_img/image50.png")
                },
                {
                    id: 8,
                    item: require("../assets/column_img/image44.png")
                },
                {
                    id: 9,
                    item: require("../assets/column_img/image48.png")
                }
            ]
        }
    },
    setup() {
        const ModalTriggers = ref({
			buttonTrigger: true
		});
		const ToggleModal = (trigger) => {
			ModalTriggers.value[trigger] = !ModalTriggers.value[trigger]
		};

        return {
            modules: [Pagination, Navigation],
            Modal,
			ModalTriggers,
			ToggleModal
        }
    }
}
</script>