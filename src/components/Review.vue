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
        </section>
    </div>
</template>