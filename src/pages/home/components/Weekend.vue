<template>
  <div>
    <div class="head">
      周末去哪儿
    </div>
    <ul>
      <li class="item" v-for="item in weekendList" :key="item.id">
        <div class="item-img">
          <img class="item-img-content" :src="item.imgUrl">
        </div>
        <div class="item-info">
          <p class="item-title">{{item.title}}</p>
          <p class="item-desc">{{item.desc}}</p>
        </div>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'HomeWeekend',
  props: {
    weekendList: Array
  }
}
</script>

<style lang="stylus" scoped>
  @import '~styles/varibles.styl'
  @import '~styles/mixins.styl'
  .head
    padding-left:.2rem
    line-height: $headerHeight
    background: #eee
  .item
    border-bottom: .07rem solid #eee
    .item-img
      overflow: hidden
      width: 100%
      height: 0
      padding-bottom: 38%
      .item-img-content
        width: 100%
    .item-info
      padding-top: .3rem
      padding-left: .22rem
      .item-title
        line-height: .2rem
      .item-desc
        line-height: .7rem
        font-size: .24rem
</style>
