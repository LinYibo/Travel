<template>
  <div class="wrapper">
    <swiper :options="swiperOption">
      <swiper-slide v-for="item of swiperList" :key="item.id">
        <img class="swiper-img" :src="item.imgUrl">
      </swiper-slide>
      <div class="swiper-pagination" slot="pagination"></div>
    </swiper>
  </div>
</template>

<script>
export default {
  name: 'HomeSwiper',
  data () {
    return {
      swiperOption: {pagination: '.swiper-pagination', loop: true},
      swiperList: [{
        id: '0001',
        imgUrl: 'http://m.elongstatic.com/promotions/wireless/uploadImages/images/158468056519228.jpg'
      }, {
        id: '0002',
        imgUrl: 'http://m.elongstatic.com/promotions/wireless/uploadImages/images/158238111739126.jpg'
      }]
    }
  }
}
</script>

<style lang="stylus" scoped>
  .wrapper >>> .swiper-pagination-bullet-active
    background #fff
  .wrapper
    overflow hidden
    width 100%
    height 0
    padding-bottom 37.33%
    background-color #eee
    .swiper-img {
      width: 100%;
}
</style>
