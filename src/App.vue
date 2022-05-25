<template>
  <div class="app">
    <Header/>
    <Promo/>
  </div>
</template>

<script>

import Header from './components/Header.vue'
import Promo from './components/Promo.vue'

export default {
  name: 'App',
  components: {
    Header,
    Promo
  }
}
</script>
