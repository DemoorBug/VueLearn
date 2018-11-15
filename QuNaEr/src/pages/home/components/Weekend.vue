<template>
  <div>
    <div class="title">热销推荐</div>
    <ul>
      <li class="item border-bottom" v-for='item of recommendList' :key="item.id">
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
  data () {
    return {
      recommendList: [{
        id: '0001',
        imgUrl: 'http://img1.qunarzz.com/sight/source/1810/92/d713ba62272715.jpg_r_640x214_88079161.jpg',
        title: '大连圣亚海洋世界',
        desc: '浪漫大连首战，浪漫的海洋主题乐园'
      }, {
        id: '0002',
        imgUrl: 'http://img1.qunarzz.com/sight/source/1810/92/d713ba62272715.jpg_r_640x214_88079161.jpg',
        title: '大连圣亚海洋世界',
        desc: '浪漫大连首战，浪漫的海洋主题乐园'
      }]
    }
  }
}
</script>

<style lang="stylus" scoped>
  @import '~styles/maxins'
  .title
    margin-top .2rem
    line-height .8rem
    background #eee
    text-indent .2rem
  .item-img-wrapper
    height 0
    overflow hidden
    padding-bottom 33.9%
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
