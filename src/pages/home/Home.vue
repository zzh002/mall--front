<template>
  <div class="home">
    <home-header></home-header>
    <home-icons></home-icons>
    <home-list></home-list>
  </div>
</template>

<script>
import HomeHeader from './components/Header'
import HomeIcons from './components/Icons'
import HomeList from './components/List'
export default {
  name: 'Home',
  components: {
    HomeHeader,
    HomeIcons,
    HomeList
  }
}
</script>

<style lang="stylus" scoped>
  .home
    position: absolute
    top: 0
    left: 0
    height: 100%
    width: 100%
</style>
