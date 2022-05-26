<template>
    <div class="images">
        <img :src=" require('../assets/column_img/' + img_data.item)" alt="review-image">
    </div>
</template>

<script>
export default {
    props: {
        img_data: {
            type: Object,
            default() {
                return{}
            }
        }
    }
}
</script>