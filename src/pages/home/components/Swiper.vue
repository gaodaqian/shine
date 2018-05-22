<template>
  <div class="wapper">
    <swiper :options="swiperOption" v-if="showSwiper">
      <swiper-slide v-for="item of list" :key="item.id">
        <img class="swiper-img" :src="item.imgUrl" alt="">
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
      }
    }
  },
  props: {
    list: Array
  },
  computed: {
    showSwiper () {
      return this.list.length
    }
  }
}
</script>
<style lang="stylus" scoped>
.wapper >>> .swiper-pagination-bullet-active
  background: #FFF
.wapper
  width: 100%
  height: 0
  overflow: hidden
  padding-bottom: 31.25%
  background-color: #eee
  .swiper-img
    width: 100%
</style>
