<template>
    <div class="wapper">
        <swiper :options="swiperOption">
            <swiper-slide v-for="item of swiperList" :key="item.id">
                <img class="swiper-img" :src="item.imgUrl" alt="">
            </swiper-slide>
            <div class="swiper-pagination"  slot="pagination"></div>
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
      swiperList: [
        {
          id: '0001',
          imgUrl: 'http://img1.qunarzz.com/piao/fusion/1804/e5/82b53c47166cfc02.jpg_750x200_0d3a0066.jpg'
        },
        {
          id: '0002',
          imgUrl: 'http://img1.qunarzz.com/piao/fusion/1804/c4/1cdd28811593b802.jpg_750x200_5fbb7c91.jpg'
        }
      ]
    }
  }
}
</script>
<style lang="stylus" scoped>
.wapper >>> .swiper-pagination-bullet-active{
    background:#FFF;
}
.wapper {
    width: 100%;
    height: 0;
    overflow: hidden;
    padding-bottom: 26.25%;
    background-color: #eee;
    .swiper-img {
        width: 100%;
    }
}
</style>
