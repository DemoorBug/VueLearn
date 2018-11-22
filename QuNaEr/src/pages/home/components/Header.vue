<template>
  <div class="header">
    <div class="header-left">
      <div class="iconfont back-icon">&#xe624;</div>
    </div>
    <div class="header-input">
      <span class="iconfont">&#xe632;</span>
      输入城市/景点
    </div>
    <router-link to='/city'>
      <div class="header-right">
        <span class="header-right-ellipsis">{{this.city}}</span>
        <span class="iconfont arrow-icon">&#xe601;</span>
      </div>
    </router-link>
  </div>
</template>

<script>
import { mapState } from 'vuex'
export default {
  name: 'HomeHeader',
  computed: {
    ...mapState(['city'])
  }
}
</script>

<style lang="stylus" scoped>
  @import '~styles/varibles'
  @import '~styles/maxins'
  .header
    display: flex
    line-height: $headerHeight
    background: $bgColor
    color: #fff
    .header-left
      width: .64rem
      float: left
      .back-icon
        text-align: center
        font-size: .4rem
    .header-input
      flex: 1
      height: .64rem
      line-height: .64rem
      color: #ccc
      margin: .12rem .2rem
      background: #fff
      border-radius: .1rem
      padding-left: .1rem
      span
        font-size: 0.3125rem
    .header-right
      min-width: 1.04rem
      padding: 0 .1rem 0 0
      float: right
      text-align: center
      color: #fff
      .header-right-ellipsis
        ellipsis()
      span
        font-size: 0.28 rem
      .arrow-icon
        font-size: .24rem

</style>
