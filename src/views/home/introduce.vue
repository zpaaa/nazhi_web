<!-- homePage -->
<template>
  <div class="business">
      <section>
        <MyHeader title='三类业务'/>
        <ul class="wrap">
          <li>
            <img src="~common/images/business.png" alt="">
            <img class='detail' src="~common/images/business_03.jpg" alt="">
          </li>
          <li>
            <img src="~common/images/business.png" alt="">

            <img class='detail' src="~common/images/business_03.jpg" alt="">
          </li>
          <li>
            <img src="~common/images/business.png" alt="">
            <img class='detail' src="~common/images/business_03.jpg" alt="">
          </li>
        </ul>
      </section>
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
      }
    }
  }
}
</script>
<style scoped lang='stylus' type='text/stylus'>
@import '~common/stylus/variable'
  .business
    display flex
    .wrap
      display flex
      justify-content space-between
      li
        width 300px
        position relative
        // text-align center
        &:hover
          img
            display none
          .detail
            display inline
        .detail
          margin-left -75px
          width 450px
          display none
          position absolute
          margin-top -209px
          z-index 999
          background #fff
        img
          width 100%
</style>
