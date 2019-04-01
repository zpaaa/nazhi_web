<!-- nav -->
<template>
  <ul class="navlist">
            <li
                v-for="(item, index) in tabList"
                :class="navNum === index ? 'ac' : ''"
                :key="index"
                @click="changeNav(index)">
                <a>{{item.text}}</a>
            </li>
        </ul>
</template>

<script>
export default {
  data () {
    return {
			navNum: 0,
			tabList: [
        {
          text: '首页',
          url: ''
        }, {
          text: '纳智AI开放产品',
          url: ''
        }, {
          text: '关于纳智',
          url: ''
        }, {
          text: '服务领域',
          url: ''
        }
      ]
    }
  },
	components: {},
	methods: {
		changeNav (n) {
			this.navNum = n
		}
	}
}

</script>
<style scoped lang='stylus' type='text/stylus'>
@import '~common/stylus/variable'
.navlist
  height 47px
  width 387px
  line-height 47px
  padding-top 26px
  display flex
  justify-content space-around
  li
    font-size 14px
    position relative
    cursor pointer
  .ac:after
    content ''
    position absolute
    bottom 0
    left 0
    background $color-blue
    width 100%
    height 2px
    animation changeNav .5s
  @keyframes changeNav
    from
        width 0
        left 50%
    to
        width 100%
        left 0
  @media screen and (max-width: 991px)
    width 350px
</style>
