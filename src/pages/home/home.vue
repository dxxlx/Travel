<template>
  <div>
    <div class="home">
      <home-header></home-header>
      <Home-swiper></Home-swiper>
      <!--<Home-swiper></Home-swiper>-->
    </div>
  </div>

</template>
<script>
  import HomeHeader from './components/Header.vue'
  import HomeSwiper from './components/Swiper.vue'
  export default {
    name:'home',
    components:{
      HomeHeader,
      HomeSwiper
    }
  }
</script>
<style>

</style>
