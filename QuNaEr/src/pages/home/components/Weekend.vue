<template>
  <div>
    <div class="title">热销推荐</div>
    <ul>
      <li class="item border-bottom" v-for='item of weekend' :key="item.id">
        <div class="item-img-wrapper">
          <img :src="item.imgUrl" class="item-img">
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
    weekend: Array
  },
  data () {
    return {
    }
  }
}
</script>

<style lang="stylus" scoped>
  @import '~styles/maxins'
  .title
    line-height .8rem
    background #eee
    text-indent .2rem
  .item-img-wrapper
    height 0
    overflow hidden
    padding-bottom 37.09%
    .item-img
      width 100%
  .item-info
    padding .1rem
    .item-title
      line-height .54rem
      font-size .32rem
      ellipsis()
    .item-desc
      line-height .4rem
      color #ccc
      ellipsis()

</style>
