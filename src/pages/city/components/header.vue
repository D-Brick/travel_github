<template>
  <div class="header">
    <router-link to="/">
      <div class="iconfont back-icon">&#xe624;</div>
    </router-link>
    城市选择
  </div>
</template>

<script>
export default {
  name: 'CityHeader'
}
</script>

<style lang="stylus" scoped>
  @import '~styles/varibles.styl'
  .header
    position: relative
    overflow: hidden
    line-height: $headerHeight
    text-align: center
    color: #fff
    background: $bgColor
    .back-icon
      position: absolute
      left: .12rem
      font-size: .4rem
      color: #fff
</style>
