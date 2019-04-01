<template>
  <div id="app">
    <NavBar/>
    <!-- <img src="./assets/logo.png"> -->
    <router-view/>
  </div>
</template>

<script>
import NavBar from 'components/NavBar/index'
export default {
  name: 'App',
  components: {
    NavBar
  }
}
</script>

<style scoped lang="stylus" type="text/stylus">
  #app
    display flex
    flex-direction column
    justify-content center

</style>
