<template>
    <section class="promo">
        <div class="promo-img">
            <img src="@/assets/image44.png" alt="">
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
            <div class="promo-descr">
                <div class="promo-descr__retail">
                    <p class="promo-descr__retail--text">Retail price</p>
                    <span class="price">14,25 $</span> <span class="old-price">15,35 $</span>
                </div>
                <div class="promo-descr__wholesale">
                    <p class="promo-descr__wholesale--text">Wholesale price</p>
                    <span class="price">12,50 $</span>
                </div>
                <button class="promo-descr__btn">
                    Buy now
                </button>
            </div>

            <hr class="promo-line">

            <div class="promo-size"></div>
        </div>
    </section>
</template>