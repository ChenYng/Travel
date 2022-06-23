<template>
  <div class="wrapper">
    <swiper :options="swiperOption">
      <swiper-slide v-for="items of swiperList" :key="items.id">
        <img class="swiper-img" :src="items.imgUrl" />
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
      swiperOption: {
        pagination: '.swiper-pagination',
        loop: true
      },
      swiperList: [{
        id: '0001',
        imgUrl: 'https://img1.qunarzz.com/sight/p0/1503/b9/b9a4593c73228f9c.water.jpg_600x330_34fa8b22.jpg'
      }, {
        id: '0002',
        imgUrl: 'https://img1.qunarzz.com/sight/p0/201308/12/36df77b68414fce8c8d65eac.jpg_600x330_acf5139a.jpg'
      }]
    }
  }
}
</script>

<style lang="stylus" scoped>
    .wrapper >>> .swiper-pagination-bullet-active
      background: #fff
  .wrapper
    overflow: hidden
    width: 100%
    height: 0
    padding-bottom: 54.9%
    background-color: #eee
    .swiper-img
      width: 100%;
</style>
