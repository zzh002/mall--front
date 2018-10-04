<template>
  <div class="icon">
    <div class="icon-left"></div>
    <div class="icon-input">
      <div class="input-category">
        <div class="category">
          <div class="category-list">
            <router-link class="itemList"
            :to="'/productList/'">
              <p>手机</p>
            </router-link>
          </div>
          <div class="category-list">
            <router-link class="itemList"
            :to="'/productList/'">
              <p>电脑</p>
            </router-link>
          </div>
        </div>
      </div>
      <div class="wrapper">
        <swiper :options="swiperOption">
          <swiper-slide>
            <img class="swiper-img" src="http://s.happymmall.com/mmall_fe/dist/resource/banner-bg.jpg" />
          </swiper-slide>
          <swiper-slide>
            <img class="swiper-img" src="http://s.happymmall.com/mmall_fe/dist/resource/banner-fe.jpg" />
          </swiper-slide>
          <swiper-slide>
            <img class="swiper-img" src="http://s.happymmall.com/mmall_fe/dist/resource/banner-fe.jpg" />
          </swiper-slide>
          <div class="swiper-pagination"  slot="pagination"></div>
        </swiper>
      </div>
    </div>
    <div class="icon-right"></div>
  </div>
</template>

<script>
export default {
  name: 'HomeIcons',
  props: {
    list: Array
  },
  data () {
    return {
      swiperOption: {
        pagination: '.swiper-pagination',
        loop: true,
        autoplay: 1000
      }
    }
  },
  computed: {
    showSwiper () {
      return this.list.length
    }
  }
}
</script>

<style lang="stylus" scoped>
  @import '~styles/mixins.styl'
  .icon
    display: flex
    .icon-left
      float: left
      width: 4.4rem
      height: 7.33rem
    .icon-input
      flex: 1
      display: flex
      .input-category
        float: left
        width: 4.8rem
        height: 7.33rem
        background #112C0
        color: #EEEEEE
        font-size: .3rem
        .category
          height: 6.5rem
          margin-left: .2rem
          margin-top: .4rem
          margin-right: .5rem
          .category-list
            line-height: .7rem
            margin-left: .2rem
            background: #000000
            .itemList
              color: #EEEEEE
      .wrapper >>> .swiper-pagination-bullet-active
        background: #fff
      .wrapper
        margin-left: .2rem
        flex: 1
        width: 16.66rem
        height: 7.33rem
        .swiper-img
          width: 16.66rem
          height: 7.33rem
    .icon-right
      float: right
      width: 4.4rem
      height: 7.33rem
</style>
