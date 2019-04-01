<!-- header -->
<template>
  <p>{{title}}</p>
</template>

<script>
export default {
  data () {
    return {
    }
  },
  props: ['title'],

  components: {}
}

</script>
<style scoped lang='stylus' type='text/stylus'>
@import '~common/stylus/variable'
p
  width 100%
  height 196px
  line-height 196px
  font-size 36px
  text-align center
  color #3f1d78
  position relative
  z-index 998
  &:before
    content ''
    position absolute
    top 50%
    left 240px
    width 210px
    height 1px
    background #3f1d78
  &:after
    content ''
    position absolute
    top 50%
    right 240px
    width 210px
    height 1px
    background #3f1d78
</style>
