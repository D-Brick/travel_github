<template>
  <div class="search">
    <input class="search-input"
           type="text"
           placeholder="请输入城市名或拼音"
           v-model="keyword">
    <div class="search-content"
         v-show="hasList()">
      <ul>
        <li class="item border-bottom"
            v-for="item of cityList"
            :key="item.id"
        >
          {{item.name}}
        </li>
        <li class="item border-bottom"
            v-show="hasCity()"
            >
              未找到匹配项
        </li>
      </ul>
    </div>
  </div>
</template>

<script>
export default {
  name: 'CitySearch',
  data () {
    return {
      keyword: '',
      cityList: [],
      timer: null
    }
  },
  props: {
    cities: Object
  },
  watch: {
    keyword () {
      if (this.timer) {
        clearTimeout(this.timer)
      }
      this.timer = setTimeout(() => {
        const result = []
        for (let item in this.cities) {
          this.cities[item].forEach((value) => {
            if (value.name.indexOf(this.keyword) > -1 ||
                value.spell.indexOf(this.keyword) > -1) {
              result.push(value)
            }
          })
        }
        this.cityList = result
      }, 100)
    }
  },
  methods: {
    hasList () {
      return this.keyword
    },
    hasCity () {
      return !this.cityList.length
    }
  }
}
</script>

<style lang="stylus" scoped>
  @import '~styles/varibles.styl'
  .search
    height: .72rem
    background: $bgColor
    padding: 0 .1rem
    .search-input
      box-sizing: border-box
      padding: 0 .1rem
      width: 100%
      line-height: .62rem
      text-align: center
      border-radius: .06rem
      color: #666
    .search-content
      position: absolute
      top: 1.58rem
      left: 0
      right: 0
      bottom: 0
      background: #fff
      z-index: 2
      .item
        padding-left: .2rem
        line-height: .7rem
</style>
