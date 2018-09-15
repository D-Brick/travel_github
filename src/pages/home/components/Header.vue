<template>
  <div class="header">
    <div class="header-left">
      <div class="iconfont back-icon">&#xe624;</div>
    </div>
    <div class="header-input">
      <span class="iconfont">&#xe632;</span>输入城市/景点/游玩主题
    </div>
    <div class="header-right">
      {{city}}<span class="iconfont arrow">&#xe62d;</span>
    </div>
  </div>
</template>

<script>
export default {
  name: 'HomeHeader',
  props: {
    city: String
  }
}
</script>

<style lang="stylus" scoped>
  @import "~styles/varibles.styl"
  .header
    display: flex
    height: .86rem
    background: $bgColor
    .header-left
      width: .64rem
      padding-right: .2rem
      color: #fff
      .back-icon
        line-height: .86rem
        text-align: center
        font-size: .4rem
        color: #fff
    .header-input
      flex: 1
      margin: .12rem 0
      padding-left: .19rem
      line-height: .62rem
      background: #fff
      border-radius: .05rem
      color: #ccc
    .header-right
      width: 1rem
      padding-left:.125rem
      padding-right:.15rem
      line-height: .86rem
      text-align: center
      color: #fff
      .arrow
        font-size: .2rem
</style>
