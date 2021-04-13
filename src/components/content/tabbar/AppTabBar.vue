<template>
  <tab-bar>
    <tab-bar-item path="/home">
      <img slot="item-icon" src="~assets/img/tabbar/home.png" alt="">
      <img slot="item-icon-sel" src="~assets/img/tabbar/home-sel.png" alt="">
      <div slot="item-title">首页</div>
    </tab-bar-item>
    <tab-bar-item path="/category">
      <img slot="item-icon" src="~assets/img/tabbar/list.png" alt="">
      <img slot="item-icon-sel" src="~assets/img/tabbar/list-sel.png" alt="">
      <div slot="item-title">列表</div>
    </tab-bar-item>
    <tab-bar-item path="/cart">
      <img slot="item-icon" src="~assets/img/tabbar/cart_empty.png" alt="">
      <img slot="item-icon-sel" src="~assets/img/tabbar/cart_empty-sel.png" alt="">
      <div slot="item-title">购物车</div>
    </tab-bar-item>
    <tab-bar-item path="/profile">
      <img slot="item-icon" src="~assets/img/tabbar/user.png" alt="">
      <img slot="item-icon-sel" src="~assets/img/tabbar/user-sel.png" alt="">
      <div slot="item-title">我的</div>
    </tab-bar-item>
  </tab-bar>
</template>

<script>
import TabBar from 'components/common/tabbar/TabBar'
import TabBarItem from 'components/common/tabbar/TabBarItem'

export default {
  name: 'AppTabBar',
  components: {
    TabBar,
    TabBarItem
  }
}
</script>

<style>

</style>