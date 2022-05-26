<template>
    <div class="carousel-track">
        <div class="carousel-item">
            <div class="carousel-item__img">
                <img :src=" require('../assets/slide_img/' + product_data.image)" alt="">
            </div>
            <div class="carousel-item__descr">
                <span class="carousel-item__descr--price">{{ product_data.price }} $ <span>{{ product_data.oldprice }} $</span></span>
                <p class="carousel-item__descr--text">{{ product_data.name }}</p>
                <a href="#" class="carousel-item__descr--link">{{ product_data.link }}</a>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    props: {
        product_data: {
            type: Object,
            default() {
                return{}
            }
        }
    }
}
</script>