<template>
  <div>
    <div class="banner" @click="handleBannerClick">
      <img src="http://img1.qunarzz.com/sight/p0/1507/36/ce3d2d6c9ab44d67ae68d940b8781829.water.jpg_600x330_f68eb231.jpg" class="banner-img">
      <div class="banner-info">
        <div class="banner-title">北京海洋馆(AAAA景区)</div>
        <div class="banner-number">
          <span class="iconfont banner-icon">&#xe616;</span>39</div>
      </div>
    </div>
    <common-gallary :imgs="imgs" v-show="showGallary" @close="handleGallaryClose"></common-gallary>
  </div>
</template>
<script>
import CommonGallary from 'common/gallary/Gallary'
export default {
  name: 'DetailBanner',
  data () {
    return {
      imgs: ['http://img1.qunarzz.com/sight/p0/1507/36/ce3d2d6c9ab44d67ae68d940b8781829.water.jpg_r_800x800_7462ee3a.jpg', 'http://img1.qunarzz.com/sight/p0/201311/07/da3ac2bcd63c36c0c8d65eac.jpg_r_800x800_4756b9d2.jpg'],
      showGallary: false
    }
  },
  components: {
    CommonGallary
  },
  methods: {
    handleBannerClick () {
      this.showGallary = true
    },
    handleGallaryClose () {
      this.showGallary = false
    }
  }
}
</script>
<style lang="stylus" scoped>
.banner
  overflow: hidden
  height: 0
  padding-bottom: 55%
  position: relative
  .banner-img
    width: 100%
  .banner-info
    display: flex
    position: absolute
    left: 0
    right: 0
    bottom: 0
    line-height: 0.6rem
    color: #fff
    background-image: linear-gradient(top, rgba(0, 0, 0, 0), rgba(0, 0, 0, 0.8))
    .banner-title
      flex: 1
      font-size: 0.32rem
      padding: 0 0.2rem
    .banner-number
      height: 0.32rem
      line-height: 0.32rem
      margin-top: 0.14rem
      padding: 0 0.4rem
      font-size: 0.24rem
      border-radius: 0.2rem
      background: rgba(0, 0, 0, 0.8)
      .banner-icon
        font-size: 0.24rem
        box-sizing: border-box
        padding-right: 0.1rem
</style>
