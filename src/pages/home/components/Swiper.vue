<template>
  <div class="wraper">
    <swiper :options="swiperOption">
      <!-- slides -->
      <swiper-slide v-for="item of swiperList" :key="item.id">
        <img class="swiper-img" :src="item.imgUrl" alt="">
      </swiper-slide>
      <!-- Optional controls -->
      <div class="swiper-pagination"  slot="pagination"></div>
    </swiper>
  </div>

</template>
<script>
  export default {
    name:'HomeSwiper',
    data(){
      return{
        swiperOption:{
          pagination:'.swiper-pagination',
          loop:true
        },
        swiperList:[
          {
            id:'001',
            imgUrl:'https://img1.qunarzz.com/vc/6a/36/df/4415fc5ed7c08d33649807f321.jpg'
          },
          {
            id:'002',
            imgUrl:'https://img1.qunarzz.com/vc/c1/c3/4f/7cd9da5aadf1c5b15cdbe11424.jpg'
          }
        ]
      }
    }
  }
</script>
<style lang="stylus" scoped>
  .wraper>>> .swiper-pagination-bullet-active
    background #fff !important
  .wraper
    overflow hidden
    width 100%
    height 0
    padding-bottom 31.25%
    background-color #eee
    .swiper-img
      width 100%
</style>
