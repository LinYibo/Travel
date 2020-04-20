<template>
  <div>
    <div class="title">周末去哪儿</div>
    <ul>
      <li v-for="item of recommendList" :key="item.id" class="item border-bottom">
        <div class="item-img-wrapper">
          <img class="item-img" :src="item.imgUrl">
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
  name: 'HomeRecommend',
  data () {
    return {
      recommendList: [{
        id: '0001',
        imgUrl: 'http://imgs.qunarzz.com/vc/6d/9f/35/b8ad5468f73fd60ec0ced086f6.jpg_92.jpg',
        title: '北海当地游 4天跟团游',
        desc: '8人小团|0购物0自费|北海+涠洲岛4日|1晚涠洲岛海边客栈+1晚北海海景房'
      }, {
        id: '0002',
        imgUrl: 'http://imgs.qunarzz.com/vc/e3/a1/71/f498dfd3bed948d623c9093252.jpg_92.jpg',
        title: '北海当地游 4天跟团游',
        desc: '8人小团|0购物0自费|北海+涠洲岛4日|1晚涠洲岛海边客栈+1晚北海海景房'
      }, {
        id: '0003',
        imgUrl: 'http://imgs.qunarzz.com/vc/44/e9/86/95bc36c9e1c06ebd68bdfe222e.jpg_92.jpg',
        title: '北海当地游 4天跟团游',
        desc: '8人小团|0购物0自费|北海+涠洲岛4日|1晚涠洲岛海边客栈+1晚北海海景房'
      }]
    }
  }
}
</script>

<style lang="stylus" scoped>
  @import '~styles/mixins.styl'
  .title
    margin-top .2rem
    line-height .8rem
    background #eee
    text-indent .2rem
  .item-img-wrapper
    overflow hidden
    height 0
    padding-bottom 30.48%
    .item-img
      width 100%
  .item-info
    padding .1rem
    .item-title
      line-height .4rem
      font-size .32rem
      ellipsis()
    .item-desc
      margin-top .03rem
      line-height .4rem
      color #ccc
      overflow hidden
      text-overflow ellipsis
      display -webkit-box
      -webkit-line-clamp 2
      -webkit-box-orient vertical;
</style>
