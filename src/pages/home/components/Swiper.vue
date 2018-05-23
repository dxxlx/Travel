<template>
  <div class="wraper">
    <swiper :options="swiperOption">
      <!-- slides -->
      <swiper-slide v-for="item of list" v-if="showSwiper" :key="item.id">
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
    props:{
      list:Array
    },
    data(){
      return{
        swiperOption:{
          pagination:'.swiper-pagination',
          loop:true
        }
      }
    },
    computed:{
      showSwiper(){
        return this.list.length
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
