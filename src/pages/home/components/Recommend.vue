<template>
  <div>
    <div class="recommeng-title">热销推荐</div>
    <ul>
      <li class="item" border-bottom v-for="item of recommendList" :key="item.id">
        <img :src="item.imgUrl" class="item-img" />
        <div class="item-info">
          <p class="item-title">{{item.title}}</p>
          <p class="item-desc">{{item.desc}}</p>
          <button class="item-button">查看详情</button>
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
        imgUrl: 'https://img1.qunarzz.com/sight/p0/201308/08/41150dacc0e3a0c8c8d65eac.jpg_256x160_14e8c382.jpg',
        title: '大连圣亚海洋世界',
        desc: '浪漫大连首站，浪漫的海洋主题公园'
      }, {
        id: '0002',
        imgUrl: 'https://img1.qunarzz.com/sight/p0/201308/08/41150dacc0e3a0c8c8d65eac.jpg_256x160_14e8c382.jpg',
        title: '大连圣亚海洋世界',
        desc: '浪漫大连首站，浪漫的海洋主题公园'
      }, {
        id: '0003',
        imgUrl: 'https://img1.qunarzz.com/sight/p0/201308/08/41150dacc0e3a0c8c8d65eac.jpg_256x160_14e8c382.jpg',
        title: '大连圣亚海洋世界',
        desc: '浪漫大连首站，浪漫的海洋主题公园'
      }]
    }
  }
}
</script>

<style lang="stylus" scoped>
  @import '~styles/mixins.styl'
  .recommeng-title
    margin-top: .2rem
    line-height: .8rem
    background: #eee
    text-index: .2rem
  .item
    display: flex
    overflow: hidden
    height: 1.9rem
  .item-img
    width: 1.7rem
    height: 1.7rem
    padding: .1rem
  .item-info
    flex: 1
    padding: .1rem
    min-width: 0
  .item-title
    line-height: .54rem
    font-size: .32rem
    ellipsis()
  .item-desc
    line-height: .4rem
    color: #ccc
  .item-button
    line-height: .44rem
    margin-top: .16rem
    background: #ff9300
    padding: 0 .2rem
    border-radius: .06rem
    color: #fff
</style>
