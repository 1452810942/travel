<template>
  <div class="wrapper">
    <swiper :options="swiperOption">
      <swiper-slide v-for="item of swiperList" :key= "item.id">
        <img class="swiper-img" :src="item.imgUrl"/>
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
      swiperList: [{
        id: '01',
        imgUrl: 'http://img1.qunarzz.com/piao/fusion/1811/af/6514cb16ed9a3402.jpg_750x200_2cb0367a.jpg'
      }, {
        id: '02',
        imgUrl: 'http://img1.qunarzz.com/piao/fusion/1804/ce/35ef931a7f692702.jpg_750x200_d04856ec.jpg'
      }]
    }
  }
}
</script>

<style lang="stylus" scoped>
.wrapper >>> .swiper-pagination-bullet-active
    background: #fff
.wrapper
    width: 100%
    height: 0
    padding-bottom: 26.7%
    background-color: #ccc
    .swiper-img
        width: 100%
</style>
