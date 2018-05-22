<template>
  <div>
    <div class="home">
      <home-header></home-header>
      <home-swiper></home-swiper>
      <home-icons></home-icons>
      <home-recommand></home-recommand>
      <home-weekend></home-weekend>
      <!--<Home-swiper></Home-swiper>-->
    </div>
  </div>

</template>
<script>
  import HomeHeader from './components/Header.vue'
  import HomeSwiper from './components/Swiper.vue'
  import HomeIcons from './components/Icons.vue'
  import HomeRecommand from './components/Recommend.vue'
  import HomeWeekend from './components/Weekend.vue'
  export default {
    name:'home',
    components:{
      HomeHeader,
      HomeSwiper,
      HomeIcons,
      HomeRecommand,
      HomeWeekend
    }
  }
</script>
<style>

</style>
