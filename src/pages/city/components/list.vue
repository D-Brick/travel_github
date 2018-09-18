<template>
  <div class="list" ref="content">
    <div>
      <div class="area">
        <div class="title border-topbottom">当前城市</div>
        <div class="button-list">
          <div class="button-wrapper">
            <div class="button">北京</div>
          </div>
        </div>
      </div>
      <div class="area">
        <div class="title border-topbottom">热门城市</div>
        <div class="button-list">
          <div class="button-wrapper">
            <div class="button">北京</div>
          </div>
          <div class="button-wrapper">
            <div class="button">上海</div>
          </div>
          <div class="button-wrapper">
            <div class="button">丽江</div>
          </div>
          <div class="button-wrapper">
            <div class="button">桂林</div>
          </div>
          <div class="button-wrapper">
            <div class="button">海南</div>
          </div>
        </div>
      </div>
      <div class="area">
        <div class="title border-topbottom">A</div>
        <ul class="city-list">
          <li class="city-item border-bottom">阿克苏</li>
          <li class="city-item border-bottom">阿克苏</li>
          <li class="city-item border-bottom">阿克苏</li>
          <li class="city-item border-bottom">阿克苏</li>
          <li class="city-item border-bottom">阿克苏</li>
          <li class="city-item border-bottom">阿克苏</li>
          <li class="city-item border-bottom">阿克苏</li>
          <li class="city-item border-bottom">阿克苏</li>
        </ul>
      </div>
      <div class="area">
        <div class="title border-topbottom">A</div>
        <ul class="city-list">
          <li class="city-item border-bottom">阿克苏</li>
          <li class="city-item border-bottom">阿克苏</li>
          <li class="city-item border-bottom">阿克苏</li>
          <li class="city-item border-bottom">阿克苏</li>
          <li class="city-item border-bottom">阿克苏</li>
          <li class="city-item border-bottom">阿克苏</li>
          <li class="city-item border-bottom">阿克苏</li>
          <li class="city-item border-bottom">阿克苏</li>
        </ul>
      </div>
    </div>
  </div>
</template>

<script>
import BScroll from 'better-scroll'
export default {
  name: 'CityList',
  mounted () {
    this.scroll = new BScroll(this.$refs.content)
  }
}
</script>

<style lang="stylus" scoped>
  @import '~styles/varibles.styl'
  .border-topbottom
    &:before
      border-color: #ccc
    &:after
      border-color: #ccc
  .list
    overflow: hidden
    position: absolute
    top: 1.58rem
    left: 0
    right: 0
    bottom: 0
    .title
      padding-left: .2rem
      line-height: .54rem
      background: #eee
      font-size: .26rem
      color: #666
    .button-list
      overflow: hidden
      padding: .1rem .6rem .1rem .1rem
      .button-wrapper
        float: left
        width: 33.33%
        .button
          box-sizing: border-box
          margin: .1rem
          padding: .1rem 0
          text-align: center
          border: .02rem solid #ccc
          border-radius: .06rem
    .city-item
      padding-left: .2rem
      line-height: .76rem
</style>
