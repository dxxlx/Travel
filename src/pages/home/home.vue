<template>
  <div>
    <div class="home">
      <home-header></home-header>
      <home-swiper></home-swiper>
      <home-icons></home-icons>
      <!--<Home-swiper></Home-swiper>-->
    </div>
  </div>

</template>
<script>
  import HomeHeader from './components/Header.vue'
  import HomeSwiper from './components/Swiper.vue'
  import HomeIcons from './components/Icons.vue'
  export default {
    name:'home',
    components:{
      HomeHeader,
      HomeSwiper,
      HomeIcons
    }
  }
</script>
<style>

</style>
