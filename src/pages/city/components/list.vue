<template>
  <div class="list">
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
</template>

<script>
export default {
  name: 'CityList'
}
</script>

<style lang="stylus" scoped>
  @import '~styles/varibles.styl'
  .border-topbottom
    &:before
      border-color: #ccc
    &:after
      border-color: #ccc
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
