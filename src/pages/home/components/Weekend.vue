<template>
  <div>
    <div class="title">周末去哪</div>
    <ul>
      <li class="item border-bottom" v-for="item of recommandList" :key="item.id">
        <div class="item-img-wrapper">
          <img class="item-img" :src="item.imgUrl" alt="">
        </div>

        <div class="item-info">
          <p class="item-title">
            {{item.title}}
          </p>
          <p class="item-desc">
            {{item.desc}}
          </p>

        </div>

      </li>
    </ul>
  </div>
</template>
<script>
  export default {
    name:'HomeWeekend',
    data(){
      return{
        recommandList:[
          {
            id:'0001',
            imgUrl:'http://img1.qunarzz.com/sight/source/1505/19/58f233e11df7ef.jpg_r_640x214_6b42c9fc.jpg',
            title:'秦始皇博物院',
            desc:'秦始皇博物院很壮观，很雄伟,厉害顶顶顶顶'
          },
          {
            id:'0002',
            imgUrl:'http://img1.qunarzz.com/sight/source/1505/19/58f233e11df7ef.jpg_r_640x214_6b42c9fc.jpg',
            title:'秦始皇博物院',
            desc:'秦始皇博物院很壮观，很雄伟,厉害顶顶顶顶'
          },
          {
            id:'0003',
            imgUrl:'http://img1.qunarzz.com/sight/source/1505/19/58f233e11df7ef.jpg_r_640x214_6b42c9fc.jpg',
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
  .item-img-wrapper
    overflow hidden
    height 0
    padding-bottom 33.9%
    .item-img
      width 100%
  .item-info
    padding .1rem
    min-width 0
    .item-title
      line-height .54rem
    .item-desc
      line-height .4rem
      color #ccc
      ellipsis()
</style>
