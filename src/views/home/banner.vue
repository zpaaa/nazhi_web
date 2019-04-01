<!-- homePage -->
<template>
  <div class="banner">
    <img src="@/common/images/banner.png" alt="">
    <div class="float_wrap">
      <button>
        立即下载
        <img src="~common/images/banner_arrow.png" alt="">
      </button>
      <a href="">技术文档</a>
      <a href="">Demo下载</a>
    </div>
  </div>
</template>

<script>
import MyHeader from 'components/Myheader'
export default {
  data () {
    return {
    }
  },
  mounted () {
    // window.addEventListener('scroll', this.handleScroll)
  },
  components: {
    MyHeader
  },
  methods: {
    handleScroll () {
      var scrollTop = document.documentElement.scrollTop || document.body.scrollTop
      console.log(scrollTop)
      if (scrollTop > 300) {
        document.getElementsByClassName('banner')[0].className = 'banner moveBanner'
        // document.getElementsByClassName('banner')[0].setAttribute('style', 'animatio: changeBanner 1s')
      }
    }
  }
}
</script>
<style scoped lang='stylus' type='text/stylus'>
@import '~common/stylus/variable'
  .banner
    // width 100vw
    margin 0 auto
    margin-bottom 30px
    position relative
    overflow hidden
    img
      display block
      overflow hidden
      width 100%
      height 100%
    .float_wrap
      position absolute
      left 49.4vw
      top 65%
      display flex
      button
        width 279px
        height 78px
        line-height 78px
        padding 0 70px 0 0
        border-radius 35px
        background $color-blue
        box-shadow  0 0 30px $color-blue
        font-size 24px
        display inline-block
        position relative
        margin-right 20px
        flex-shrink 0
        img
          width 62px
          height 62px
          position absolute
          right 8px
          top 8px
      a
        display block
        line-height 39px
        height 39px
        color $color-blue
        margin 20px
        border-bottom 2px solid $color-blue
        flex-shrink 0
  // 平板
  @media screen and (max-width: 991px)
    .banner
      .float_wrap
        button
          width 129px
          height 38px
          line-height 38px
          padding 0 40px 0 0
          border-radius 20px
          background $color-blue
          box-shadow  0 0 30px $color-blue
          font-size 14px
          display inline-block
          position relative
          margin-right 10px
          flex-shrink 0
          img
            width 32px
            height 32px
            position absolute
            right 4px
            top 2px
        a
          display block
          line-height 35px
          height 35px
          font-size 14px
          color $color-blue
          margin 10px
          margin-top 0px
          border-bottom 2px solid $color-blue
          flex-shrink 0
</style>
