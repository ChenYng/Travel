<template>
  <div>
    <div class="banner" @click="handleBannerClick">
      <img class="banner-img" :src="bannerImg" />
      <div class="banner-info">
        <div class="banner-title">
          {{this.sightName}}
        </div>
        <div class="banner-number">
          <span class="iconfont">&#xe692;</span>
          {{this.bannerImgs.length}}
        </div>
      </div>
    </div>
    <fade-animation>
      <common-gallery :imgs="bannerImgs" v-show="showGallery" @close="handleGalleryClose"></common-gallery>
    </fade-animation>
  </div>
</template>

<script>
import CommonGallery from 'common/gallery/Gallery.vue'
import FadeAnimation from 'common/fade/FadeAnimation.vue'
export default {
  name: 'DetailBanner',
  props: {
    sightName: String,
    bannerImg: String,
    bannerImgs: Array
  },
  data () {
    return {
      showGallery: false
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
    CommonGallery,
    FadeAnimation
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
