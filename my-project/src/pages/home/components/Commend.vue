<template>
  <div>
    <div class="title">热门榜单</div>
    <ul>
      <li class="item border-bottom" v-for="item of commendList" :key="item.id">
        <img class="commend-img" :src="item.imgUrl" />
        <div class="commend-font">
          <p class="font-title">{{item.title}}</p>
          <p class="font-desc">{{item.desc}}</p>
          <button class="font-button">查看详细</button>
        </div>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'HomeCommend',
  data () {
    return {
      commendList: [{
        id: '001',
        imgUrl: 'http://img1.qunarzz.com/sight/p0/201404/23/04b92c99462687fa1ba45c1b5ba4ad77.jpg_350x240_4dd46cd0.jpg',
        title: '大连圣亚海洋世界',
        desc: '浪漫大连首站，浪漫的海洋主题公园'
      }, {
        id: '002',
        imgUrl: 'http://img1.qunarzz.com/sight/p0/201404/23/04b92c99462687fa1ba45c1b5ba4ad77.jpg_350x240_4dd46cd0.jpg',
        title: '大连圣亚海洋世界',
        desc: '浪漫大连首站，浪漫的海洋主题公园'
      }, {
        id: '003',
        imgUrl: 'http://img1.qunarzz.com/sight/p0/201404/23/04b92c99462687fa1ba45c1b5ba4ad77.jpg_350x240_4dd46cd0.jpg',
        title: '大连圣亚海洋世界',
        desc: '浪漫大连首站，浪漫的海洋主题公园'
      }, {
        id: '004',
        imgUrl: 'http://img1.qunarzz.com/sight/p0/201404/23/04b92c99462687fa1ba45c1b5ba4ad77.jpg_350x240_4dd46cd0.jpg',
        title: '大连圣亚海洋世界',
        desc: '浪漫大连首站，浪漫的海洋主题公园'
      }]
    }
  }
}
</script>

<style lang="stylus" scoped>
@import '~styles/minux.styl'
.title
    height: .8rem
    line-height: .8rem
    margin-top: .2rem
    background-color: #eee
    text-indent: .2rem
.item
    display: flex
    height: 1.9rem
    overflow: hidden
    min-width: 0
    .commend-img
        width: 1.7rem
        height: 1.7rem
        padding: .1rem
    .commend-font
        flex: 1
        margin-top: .2rem
        .font-title
            line-height: .54rem
            font: .32rem
            font-weight: 600
            ellipsis()
        .font-desc
            line-height: .4rem
            color: #ccc
            ellipsis()
        .font-button
            background-color: #ff9300
            border-radius: .06rem
            padding: 0 .2rem
            margin-top: .2rem
            color: #fff
            line-height: .46rem
</style>
