<template>
  <div class="icon">
    <div class="icon-left"></div>
    <div class="icon-input">
      <div class="input-category">
        <div class="category">
          <div class="category-list"
          v-for="List of categoryList"
          :key="List.id">
            <router-link class="itemList"
            :to="'/productList/'+item.categoryName"
            v-for="item of List.childList"
            :key="item.id">
              <p class="title">{{item.categoryName}}</p>
            </router-link>
          </div>
        </div>
      </div>
      <div class="wrapper">
        <swiper :options="swiperOption">
          <swiper-slide
          v-for="item of imgUrlList"
          :key="item.id">
            <img class="swiper-img" :src="item.imgUrl" />
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
      },
      categoryList: [{
        id: '0001',
        childList: [{
          id: '0011',
          categoryName: '手机'
        }, {
          id: '0012',
          categoryName: '数码'
        }, {
          id: '0013',
          categoryName: '电脑'
        }]
      }, {
        id: '0002',
        childList: [{
          id: '0011',
          categoryName: '手机'
        }, {
          id: '0012',
          categoryName: '数码'
        }, {
          id: '0013',
          categoryName: '电脑'
        }]
      }, {
        id: '0003',
        childList: [{
          id: '0011',
          categoryName: '手机'
        }, {
          id: '0012',
          categoryName: '数码'
        }, {
          id: '0013',
          categoryName: '电脑'
        }]
      }, {
        id: '0005',
        childList: [{
          id: '0011',
          categoryName: '手机'
        }, {
          id: '0012',
          categoryName: '数码'
        }, {
          id: '0013',
          categoryName: '电脑'
        }]
      }, {
        id: '0006',
        childList: [{
          id: '0011',
          categoryName: '手机'
        }, {
          id: '0012',
          categoryName: '数码'
        }, {
          id: '0013',
          categoryName: '电脑'
        }]
      }, {
        id: '0007',
        childList: [{
          id: '0011',
          categoryName: '手机'
        }, {
          id: '0012',
          categoryName: '数码'
        }, {
          id: '0013',
          categoryName: '电脑'
        }]
      }, {
        id: '0008',
        childList: [{
          id: '0011',
          categoryName: '手机'
        }, {
          id: '0012',
          categoryName: '数码'
        }, {
          id: '0013',
          categoryName: '电脑'
        }]
      }, {
        id: '0009',
        childList: [{
          id: '0011',
          categoryName: '手机'
        }, {
          id: '0012',
          categoryName: '数码'
        }, {
          id: '0013',
          categoryName: '电脑'
        }]
      }, {
        id: '0010',
        childList: [{
          id: '0011',
          categoryName: '手机'
        }, {
          id: '0012',
          categoryName: '数码'
        }, {
          id: '0013',
          categoryName: '电脑'
        }]
      }, {
        id: '0008',
        childList: [{
          id: '0011',
          categoryName: '手机'
        }, {
          id: '0012',
          categoryName: '数码'
        }, {
          id: '0013',
          categoryName: '电脑'
        }]
      }, {
        id: '0009',
        childList: [{
          id: '0011',
          categoryName: '手机'
        }, {
          id: '0012',
          categoryName: '数码'
        }, {
          id: '0013',
          categoryName: '电脑'
        }]
      }, {
        id: '0010',
        childList: [{
          id: '0011',
          categoryName: '手机'
        }, {
          id: '0012',
          categoryName: '数码'
        }, {
          id: '0013',
          categoryName: '电脑'
        }]
      }],
      imgUrlList: [{
        id: '001',
        imgUrl: 'https://m.360buyimg.com/babel/jfs/t25450/4/1365535286/92069/6ccbe1b6/5baf25f2N25055c8f.jpg'
      }, {
        id: '002',
        imgUrl: 'https://m.360buyimg.com/babel/jfs/t25357/311/1418178055/56438/3ea26ff6/5bb06d6bN840dd018.jpg'
      }, {
        id: '003',
        imgUrl: 'https://img1.360buyimg.com/pop/jfs/t27019/62/461506351/100035/471b46d2/5baf1cf1N021c6fc6.jpg'
      }, {
        id: '004',
        imgUrl: 'https://m.360buyimg.com/babel/jfs/t26557/57/490361443/40488/1cda9ffc/5bafc32dNf083ecb3.jpg'
      }, {
        id: '005',
        imgUrl: 'https://img1.360buyimg.com/pop/jfs/t26671/108/526518700/185543/96bc53ab/5bb07bccN8ea43371.jpg'
      }]
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
        background #757575
        font-size: .3rem
        .category
          height: 6.5rem
          margin-left: .2rem
          margin-top: .26rem
          margin-right: .5rem
          .category-list
            line-height: .7rem
            margin-left: .1rem
            .itemList
              color: #EEEEEE
              float: left
              position: relative
              width: 30%
      .wrapper >>> .swiper-pagination-bullet-active
        background: #fff
      .wrapper
        margin-left: .2rem
        flex: 1
        overflow: hidden
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
