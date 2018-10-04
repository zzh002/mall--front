<template>
  <div class="home">
    <home-header></home-header>
    <home-icons></home-icons>
    <home-list></home-list>
    <home-footer></home-footer>
  </div>
</template>

<script>
import HomeHeader from './components/Header'
import HomeIcons from './components/Icons'
import HomeList from './components/List'
import HomeFooter from './components/Footer'
export default {
  name: 'Home',
  components: {
    HomeHeader,
    HomeIcons,
    HomeList,
    HomeFooter
  }
}
</script>

<style lang="stylus" scoped>
  .home
    background: #EEEEEE
</style>
