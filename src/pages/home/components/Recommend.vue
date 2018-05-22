<template>
  <div>
    <div class="title">热门推荐</div>
    <ul>
      <li class="item border-bottom" v-for="item of recommandList" :key="item.id">
        <img class="item-img" :src="item.imgUrl" alt="">
        <div class="item-info">
          <p class="item-title">
            {{item.title}}
          </p>
          <p class="item-desc">
            {{item.desc}}
          </p>
          <button class="item-button">查看详情</button>
        </div>

      </li>
    </ul>
  </div>
</template>
<script>
  export default {
    name:'HomeRecommand',
    data(){
      return{
        recommandList:[
          {
            id:'0001',
            imgUrl:'http://img1.qunarzz.com/sight/p0/1411/1a/5582f9f24bc50b475a8cbda4c5ac8d24.water.jpg_150x150_7e9090b5.jpg',
            title:'秦始皇博物院',
            desc:'秦始皇博物院很壮观，很雄伟,厉害顶顶顶顶'
          },
          {
            id:'0002',
            imgUrl:'http://img1.qunarzz.com/sight/p0/1411/1a/5582f9f24bc50b475a8cbda4c5ac8d24.water.jpg_150x150_7e9090b5.jpg',
            title:'秦始皇博物院',
            desc:'秦始皇博物院很壮观，很雄伟,厉害顶顶顶顶'
          },
          {
            id:'0003',
            imgUrl:'http://img1.qunarzz.com/sight/p0/1411/1a/5582f9f24bc50b475a8cbda4c5ac8d24.water.jpg_150x150_7e9090b5.jpg',
            title:'秦始皇博物院',
            desc:'秦始皇博物院很壮观，很雄伟,厉害顶顶顶顶'
          }
        ]
      }
    }

  }
</script>
<style lang="stylus" scoped>
  @import "../../../assets/style/mixins.styl"
  .title
    line-height .8rem
    text-indent .2rem
    background #eee
    margin-top .2rem
  .item
    display flex
    height 1.9rem
    overflow hidden
    .item-img
      width 1.7rem
      height 1.7rem
      padding .1rem
    .item-info
      flex 1
      padding .1rem
      min-width 0
      .item-title
        line-height .54rem
      .item-desc
        line-height .4rem
        color #ccc
        ellipsis()
      .item-button
        line-height .44rem
        margin-top .2rem
        background #ff9300
        padding 0 .2rem
        border-radius .06rem
        color #fff
</style>
