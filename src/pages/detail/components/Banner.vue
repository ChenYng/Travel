<template>
  <div>
    <div class="banner" @click="handleBannerClick">
      <img class="banner-img" src="https://imgs.qunarzz.com/sight/p0/1603/87/87146cf32fa8635e90.water.png_1190x550_334f4ef5.png" />
      <div class="banner-info">
        <div class="banner-title">
          大连圣亚海洋世界（AAAA景区）
        </div>
        <div class="banner-number">
          <span class="iconfont">&#xe692;</span>
          39
        </div>
      </div>
    </div>
    <common-gallery :imgs="imgs" v-show="showGallery" @close="handleGalleryClose"></common-gallery>
  </div>
</template>

<script>
import CommonGallery from 'common/gallery/Gallery.vue'
export default {
  name: 'DetailBanner',
  data () {
    return {
      showGallery: false,
      imgs: ['https://imgs.qunarzz.com/sight/p0/1603/87/87146cf32fa8635e90.water.png_710x360_78e8d124.png', 'https://imgs.qunarzz.com/sight/p0/1902/ec/ec4d1d341fb67d1ba3.img.jpg_1190x550_f3f4d5ee.jpg']
    }
  },
  methods: {
    handleBannerClick () {
      this.showGallery = true
    },
    handleGalleryClose () {
      this.showGallery = false
    }
  },
  components: {
    CommonGallery
  }
}</script>

<style lang="stylus" scoped>
.banner
  position: relative
  overflow: hidden
  height: 0
  padding-bottom: 55%
.banner-img
  width: 100%
.banner-info
  display: flex
  position: absolute
  left: 0
  right: 0
  bottom: 0
  line-height: .6rem
  color: #fff
  background-image: linear-gradient(top,rgba(0,0,0,0),rgba(0,0,0,0.8))
.banner-title
  flex: 1
  font-size: .32rem
  padding: 0 .2rem
.banner-number
  padding: 0 .4rem
  margin-top: .2rem
  height: .32rem
  line-height: .32rem
  border-radius: .2rem
  background: rgba(0,0,0,.8)
  font-size: .24rem
.banner-icon
  font-size: .24rem
</style>
