<template>
  <div>
    <div class="banner" @click="handleBannerClick">
      <img class="banner-img" src="http://img1.qunarzz.com/sight/p0/1505/18/18ffcca94b1b7ca2.water.jpg_600x330_cd78f1b7.jpg" alt="">
      <div class="banner-info">
        <div class="banner-title">
          长恨歌
        </div>
        <div class="banner-number">
          <span class="iconfont banner-icon">&#xe626;</span>
          39
        </div>
      </div>
    </div>
    <comman-gallery :imgs="imgs" v-show="showGallery" @close="handleGalleryClose"></comman-gallery>
  </div>

</template>
<script>
  import  CommanGallery from 'comman/gallery/Gallery'
  export default {
    name:'DetailBanner',
    data(){
      return{
        showGallery:false,
        imgs:['http://img1.qunarzz.com/sight/p0/1706/73/7349ea5c85af9d5ea3.img.png_r_800x800_2afd15e0.png','http://img1.qunarzz.com/sight/p0/1706/4d/4dc144af8b342ad2a3.img.png_r_800x800_740c4665.png']
      }
    },
    methods:{
      handleBannerClick(){
        this.showGallery=true
      },
      handleGalleryClose(){
        this.showGallery=false
      }
    },
    components:{
      CommanGallery
    }
  }
</script>
<style lang="stylus" scoped>
  .banner
    position relative
    overflow hidden
    height 0
    padding-bottom 55%
    .banner-img
      width 100%
    .banner-info
      display flex
      position absolute
      left 0
      right 0
      bottom 0rem
      line-height .6rem
      color #fff
      background-image linear-gradient(top,rgba(0,0,0,0),rgba(0,0,0,0.8))
      .banner-title
        flex 1
        font-size .32rem
        padding 0 .2rem
      .banner-number
        margin-top .14rem
        padding 0 .4rem
        line-height .32rem
        height .32rem
        border-radius .2rem
        background rgba(0,0,0,.8)
        font-size .24rem
        .banner-icon
          font-size .24rem
</style>
