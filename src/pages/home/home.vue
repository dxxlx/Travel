<template>
  <div>
    <div class="home">
      <home-header :city="city"></home-header>
      <home-swiper :list="swiperList"></home-swiper>
      <home-icons :list="iconList"></home-icons>
      <home-recommand :list="recommanList"></home-recommand>
      <home-weekend :list="HomeWeekend"></home-weekend>
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
  import axios from 'axios'
  export default {
    name:'home',
    components:{
      HomeHeader,
      HomeSwiper,
      HomeIcons,
      HomeRecommand,
      HomeWeekend
    },
    data(){
      return{
        city:'',
        swiperList:[],
        iconList:[],
        recommanList:[],
        HomeWeekend:[]
      }
    },
    methods:{
      getHomeInfo(){
        console.log(2)
        axios.get('/api/index.json')
          .then(this.getHomeInfoSucc)
      },
      getHomeInfoSucc(res){
//        console.log(1)
        res=res.data
        if(res.ret && res.data){
          const data=res.data
          this.city=data.city
          this.swiperList=data.swiperList
          this.iconList=data.iconList
          this.recommanList=data.recommendList
          this.HomeWeekend=data.weekendList
        }
        console.log(res)
      }
    },
    mounted(){
      this.getHomeInfo()
    }
  }
</script>
<style>

</style>
