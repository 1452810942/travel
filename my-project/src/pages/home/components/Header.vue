<template>
    <div class="header">
        <div class="header-left">
            <div class="iconfont back-icon">&#xe624;</div>
        </div>
        <div class="header-input">
            <span class="iconfont back">&#xe632;</span>
            输入城市/景点/游玩主题
        </div>
        <div class="header-right">
            城市11
            <span class="iconfont arrow-icon">&#xe6aa;</span>
        </div>
    </div>
</template>

<script>
export default {
  name: 'HomeHeader'
}
</script>

<style lang="stylus" scoped>
@import '~styles/avaliable.styl'
.header
    line-height: .86rem
    background-color: $bgcolor
    text-align: center
    color: #fff
    display: flex
    .header-left
        width: .64rem
        float: left
        .back-icon
            font-size: .4rem
    .header-input
        flex: 1
        border-radius: .06rem
        background-color: #fff
        color: #ccc
        margin-top: .12rem
        margin-left: .2rem
        line-height: .64rem
        height: .64rem
        text-align: left
        padding-left: .20rem
    .header-right
        width: 1.24rem
        float: right
        .arrow-icon
            font-size: .24rem
            margin-left: -.05rem
</style>
