<template>
  <div>
    <div class="head">
      热销推荐
    </div>
    <ul>
      <li class="item border-bottom" v-for="item in recommendList" :key="item.id">
        <div class="item-img">
          <img class="item-img-content" :src="item.imgUrl">
        </div>
        <div class="item-info">
          <p class="item-title">{{item.title}}</p>
          <p class="item-desc">{{item.desc}}</p>
          <button class="item-button">查看详情</button>
        </div>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'HomeRecommend',
  props: {
    recommendList: Array
  }
}
</script>

<style lang="stylus" scoped>
  @import '~styles/varibles.styl'
  @import '~styles/mixins.styl'
  .head
    margin-top: .15rem
    padding-left:.2rem
    line-height: $headerHeight
    background: #eee
  .item
    display: flex
    overflow: hidden
    height: 1.9rem
    .item-img
      width: 1.7rem
      padding: .1rem
      .item-img-content
        width: 100%
    .item-info
      flex: 1
      padding-top: .2rem
      padding-left: .1rem
      min-width: 0
      .item-title
        font-size: .32rem
        ellipsis()
      .item-desc
        margin-top: .13rem
        font-size: .3rem
        color: #ccc
        ellipsis()
      .item-button
        margin-top: .17rem
        padding: 0 .15rem
        background: #ff9300
        font-size: .29rem
        color: #fff
        border-radius: .05rem
</style>
