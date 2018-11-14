<template>
  <swiper opation="HomeIcon">
    <swiper-slide v-for="(page,index) of pages" :key="index">
      <div class="icons">
        <div class="icon" v-for="item of page" :key="item.id">
            <div class="icon-img">
              <img  class="icon-img-content" :src="item.imgUrl">
            </div>
            <p class="icon-font">{{item.desc}}</p>
        </div>
      </div>
    </swiper-slide>
  </swiper>
</template>

<script>
export default {
  name: 'HomeIcon',
  data () {
    return {
      swiperOpation: {
        pagnation: 'HomeIcon'
      },
      iconList: [{
        id: '001',
        imgUrl: 'http://img1.qunarzz.com/piao/fusion/1803/95/f3dd6c383aeb3b02.png',
        desc: '景点门票'
      }, {
        id: '002',
        imgUrl: 'http://img1.qunarzz.com/piao/fusion/1803/96/c70f1e85ae4a4f02.png',
        desc: '自然风光'
      }, {
        id: '003',
        imgUrl: 'https://img1.qunarzz.com/piao/fusion/1803/20/831d62d2e1c7be02.png',
        desc: '打卡圣地'
      }, {
        id: '004',
        imgUrl: 'http://img1.qunarzz.com/piao/fusion/1803/ab/6f7d6e44963c9302.png',
        desc: '泡温泉'
      }, {
        id: '005',
        imgUrl: 'http://img1.qunarzz.com/piao/fusion/1803/80/416c6ab3368d1f02.png',
        desc: '全部玩乐'
      }, {
        id: '006',
        imgUrl: 'http://img1.qunarzz.com/piao/fusion/1803/96/c70f1e85ae4a4f02.png',
        desc: '自然风光'
      }, {
        id: '007',
        imgUrl: 'http://img1.qunarzz.com/piao/fusion/1803/95/f3dd6c383aeb3b02.png',
        desc: '景点门票'
      }, {
        id: '008',
        imgUrl: 'http://img1.qunarzz.com/piao/fusion/1803/95/f3dd6c383aeb3b02.png',
        desc: '景点门票'
      }, {
        id: '009',
        imgUrl: 'http://img1.qunarzz.com/piao/fusion/1803/95/f3dd6c383aeb3b02.png',
        desc: '景点门票'
      }]
    }
  },
  computed: {
    pages () {
      const pages = []
      this.iconList.forEach((item, index) => {
        const page = Math.floor(index / 8)
        if (!pages[page]) {
          pages[page] = []
        }
        pages[page].push(item)
      })
      return pages
    }
  }
}
</script>

<style lang="stylus" scoped>
@import '~styles/avaliable.styl'
@import '~styles/minux.styl'
.icons >>> .swiper-container
    height: 0
    padding-bottom: 50%
.icons
  margin-top: .2rem
  .icon
     position: relative
     overflow: hidden
     float: left
     width: 25%
     height: 0
     padding-bottom: 25%
     .icon-img
         position: absolute
         left: 0
         right: 0
         top: 0
         bottom: .44rem
         .icon-img-content
             display: block
             margin: 0 auto
             height: 100%
     .icon-font
         position: absolute
         left: 0
         right: 0
         bottom: 0
         height: .44rem
         line-height: .44rem
         color: $darktextcolor
         text-align: center
         ellipsis()
</style>
