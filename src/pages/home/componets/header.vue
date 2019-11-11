<template>
    <div class="header">
        <div class="header-left">
            <div class="iconfont back-icon">&#xe61f;</div>
        </div>
        <div class="header-input">
            <span class="iconfont">&#xe610;</span>
            输入城市/景点/游玩主题
        </div>
        <div class="header-right">
            城市
            <span class="iconfont arrow-icon">&#xe612;</span>
        </div>
    </div>
</template>

<script>
export default {
    name:'HomeHeader'
}
</script>
<style lang="stylus" scoped>
 @import '~styles/varibles.styl'
  .header
    background: $bgColor
    display: flex
    line-height 2.9rem
    background: #00afc7
    color: #fff
    .header-left
      width: 2.4rem
      float: left
      .back-icon
        text-align: center
        font-size: .4rem
    .header-input
      flex: 1
      height: 2.0rem
      line-height: 2.0rem
      margin-top: .3rem
      margin-left: .2rem
      padding-left: .2rem
      background: #fff
      border-radius: .1rem
      color: #ccc
      text-indent 0.5rem
    .header-right
      min-width: 1.04rem
      padding: 0 .1rem
      float: right
      text-align: center
      color: #fff
      width: 4.4rem
      .arrow-icon
        margin-left: -.04rem
        font-size: .24rem
</style>