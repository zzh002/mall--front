<template>
  <div class="header">
    <div class="header-login">
      <div class="header-left"></div>
      <div class="header-input">
        <div class="link">
          <router-link to="/">
            <a class="input-login">登陆</a>
          </router-link>
          <router-link to="/">
            <a class="input-register">注册</a>
          </router-link>
        </div>
        <div class="input">
          <router-link to="/">
            <div class="cart">
              <span class="iconfont back-icon">&#xe6b8;</span>
              购物车
            </div>
          </router-link>
          <router-link to="/">
            <div class="order">我的订单</div>
          </router-link>
          <router-link to="/">
            <div class="inform">个人中心</div>
          </router-link>
          <router-link to="/">
            <div class="connect">联系我们</div>
          </router-link>
        </div>
      </div>
      <div class="header-right"></div>
    </div>
    <div class="search">
      <div class="search-left">
        <div class="left-blank"></div>
        <div class="left-descript">M商城</div>
      </div>
      <div class="search-input">
        <input class="input"
        placeholder="请输入商品名称"
        v-model="value"/>
        <router-link to="/search/">
          <div class="button">搜索</div>
        </router-link>
      </div>
      <div class="search-right"></div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'HomeHeader',
  data () {
    return {
      value: ''
    }
  }
}
</script>

<style lang="stylus" scoped>
  .header
    height: 2.86rem
    .header-login
      display: flex
      line-height: .6rem
      background: #D5D8DC
      font-size: .25rem
      .header-left
        width: 4.4rem
        float: left
      .header-input
        flex: 1
        display: flex
        line-height: .5rem
        .link
          flex: 1
          .input-login
            width: .72rem
            color: #B71C1C
          .input-register
            width: .72rem
            color: #B71C1C
        .input
          display: flex
          width: 5.7rem
          float: right
          text-align: center
          .cart
            width: 1.425rem
            color: #B71C1C
            .back-icon
              text-align: center
              font-size: .25rem
          .order
            width: 1.425rem
            color: #B71C1C
          .inform
            width: 1.425rem
            color: #B71C1C
          .connect
            width: 1.425rem
            color: #B71C1C
      .header-right
        width: 4.4rem
        float: right
    .search
      height: 2.26rem
      display: flex
      .search-left
        width: 9.34rem
        float: left
        display: flex
        .left-blank
          width: 5.2rem
          float: left
        .left-descript
          width: 4.14rem
          float: right
          line-height: 2.2rem
          font-size: 0.8rem
          color: #B71C1C
      .search-input
        width: 13.2rem
        flex: 1
        height: .84rem
        line-height: .84rem
        margin-top: .74rem
        text-align: center
        background: #B71C1C
        display: flex
        .input
          flex: 1
          height: .67rem
          width: 13.14rem
          margin-top: .1rem
          margin-left: .1rem
          margin-bottom: .1rem
          line-height: .8rem
          background: #F9FBE7
        .button
          width: 1.78rem
          color: #FAFAFA
      .search-right
        float: right
        width: 8rem
</style>
