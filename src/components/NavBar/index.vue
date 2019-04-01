<!-- nav -->
<template>
  <div class="nav">
      <section>
        <div class="logo">
            <img src="@/common/images/logo_02.jpg" alt="">
        </div>
        <NvaList/>
      </section>
  </div>
</template>

<script>
import NvaList from './NavList'
export default {
  data () {
    return {

    }
  },
	components: {
    NvaList
  },
	methods: {
		changeNav (n) {
			this.navNum = n
		}
	}
}

</script>
<style scoped lang='stylus' type='text/stylus'>
@import '~common/stylus/variable'
.nav
    height 100px
    display flex
    justify-content center
    border-bottom 1px solid #e5e5e5
    section
        display flex
        justify-content space-between
        img
            height 100px
@media screen and (max-width: 991px)  //<=991px的设备
  .nav
    padding 20px
@media screen and (max-width: 767px) //<=767px的设备
  .nav
    display none
</style>
