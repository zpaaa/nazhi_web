<!-- homePage -->
<template>
  <div>
    <Banner></Banner>
    <Business></Business>
    <Introduce></Introduce>
  </div>
</template>
<script>
import Banner from './banner'
import Business from './business'
import Introduce from './Introduce'
export default {
  data () {
    return {
    }
  },
  mounted () {
    // window.addEventListener('scroll', this.handleScroll)
  },
  components: {
    Banner,
    Business,
    Introduce
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
    justify-content center
    .wrap
      display flex
      justify-content space-between
      li
        width 300px
        img
          width 100%
</style>
