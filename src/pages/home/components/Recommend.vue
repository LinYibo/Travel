<template>
  <div>
    <div class="title">热销推荐</div>
    <ul>
      <li v-for="item of recommendList" :key="item.id" class="item border-bottom">
        <img class="item-img" :src="item.imgUrl">
        <div class="item-info">
          <p class="item-title">{{item.title}}</p>
          <p class="item-desc">{{item.desc}}</p>
          <button class="item-btn">查看详情</button>
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
        imgUrl: 'http://imgs.qunarzz.com/vs_ceph_b2c_001/41bf7b2f-1d10-44ee-9335-0766fd920ea9.jpg_r_480x320x95_1715044e.jpg',
        title: '北海当地游 4天跟团游',
        desc: '8人小团|0购物0自费|北海+涠洲岛4日|1晚涠洲岛海边客栈+1晚北海海景房'
      }, {
        id: '0002',
        imgUrl: 'http://imgs.qunarzz.com/vs_ceph_b2c_001/41bf7b2f-1d10-44ee-9335-0766fd920ea9.jpg_r_480x320x95_1715044e.jpg',
        title: '北海当地游 4天跟团游',
        desc: '8人小团|0购物0自费|北海+涠洲岛4日|1晚涠洲岛海边客栈+1晚北海海景房'
      }, {
        id: '0003',
        imgUrl: 'http://imgs.qunarzz.com/vs_ceph_b2c_001/41bf7b2f-1d10-44ee-9335-0766fd920ea9.jpg_r_480x320x95_1715044e.jpg',
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
  .item
    display flex
    height 1.9rem
    overflow hidden
    .item-img
      width 1.7rem
      height 1.7rem
      padding .1rem
    .item-info
      flex 1
      padding .1rem
      min-width 0
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
      .item-btn
        line-height .4rem
        margin-top .06rem
        background #ff9300
        padding 0 .2rem
        border-radius .06rem
        color #fff
</style>
