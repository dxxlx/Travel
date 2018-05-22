<template>
    <div class="header">
      <div class="header-left">
        <span class="iconfont back-icon">&#xe624;</span>
      </div>
      <div class="header-input">
        <span class="iconfont">&#xe632;</span>
        输入城市/景点/游玩主题
      </div>
      <div class="header-right">
        城市
        <span class="iconfont arrow-icon">&#xe65e;</span>
      </div>
    </div>
</template>
<script>
  export default {
    name:'HomeHeader'
  }
</script>
<style lang="stylus" scoped>
  @import '../../../assets/style/variavle.styl';
  .header
    display flex
    line-height .86rem
    color #fff
    height .86rem
    background $bgcolor
    .header-left
      float left
      width .64rem
      text-align center
      font-size .4rem
    .header-input
      flex 1
      margin-top .12rem
      margin-left .2rem
      padding-left .2rem
      height .64rem
      line-height .64rem
      background #fff
      border-radius .1rem
      color #ccc
    .header-right
      width 1.24rem
      float right
      text-align center
      .arrow-icon
        margin-left -.04rem
        font-size .24rem


</style>
