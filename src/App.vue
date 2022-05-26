<template>
  <div class="app">
    <Header/>
    <Promo/>
    <Description/>
    <Carousel/>
    <Review/>
  </div>
</template>

<script>

import Header from './components/Header.vue'
import Promo from './components/Promo.vue'
import Description from './components/Description.vue'
import Carousel from './components/Carousel.vue'
import Review from './components/Review.vue'

export default {
  name: 'App',
  components: {
    Header,
    Promo,
    Description,
    Carousel,
    Review  
  }
}
</script>
