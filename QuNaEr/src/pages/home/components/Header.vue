<template>
  <div class="header">
    <div class="header-left">
      <div class="iconfont back-icon">&#xe624;</div>
    </div>
    <div class="header-input">
      <span class="iconfont">&#xe632;</span>
      输入城市/景点
    </div>
    <div class="header-right">
      <span>{{this.city}}</span>
      <span class="iconfont arrow-icon">&#xe601;</span>
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
  @import '~styles/varibles'
  .header
    display: flex
    line-height: .86rem
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
      width: 1.24rem
      float: right
      text-align: center
      span
        font-size: 0.28 rem
      .arrow-icon
        font-size: .24rem

</style>
