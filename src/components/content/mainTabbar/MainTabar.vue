<template>
   <tab-bar>
      <tab-bar-item path='/home' >
      <!-- dom中使用别名需要加~ -->
        <img slot="item-icon" src="~assets/img/tabbar/home/home.svg" alt="">
        <img slot="item-icon_active" src="~assets/img/tabbar/home/home_active.svg" alt="">
        <div slot="item-text">首页</div>
        <!-- <div>首页</div> -->
      </tab-bar-item>
      <tab-bar-item path='/category' >
        <img slot="item-icon" src="~/assets/img/tabbar/category/category.svg" alt="">
        <img slot="item-icon_active" src="~/assets/img/tabbar/category/category_active.svg" alt="">
        <div slot="item-text">分类</div>
        <!-- <div>首页</div> -->
      </tab-bar-item>
      <tab-bar-item path='/cart' >
        <img slot="item-icon" src="~/assets/img/tabbar/shopcart/shopcart.svg" alt="">
        <img slot="item-icon_active" src="~/assets/img/tabbar/shopcart/shopcart_active.svg" alt="">
        <div slot="item-text">购物车</div>
        <!-- <div>首页</div> -->
      </tab-bar-item>
      <tab-bar-item path='/profile' >
        <img slot="item-icon" src="~/assets/img/tabbar/profile/profile.svg" alt="">
        <img slot="item-icon_active" src="~/assets/img/tabbar/profile/profile_active.svg" alt="">
        <div slot="item-text">我的</div>
        <!-- <div>首页</div> -->
      </tab-bar-item>
    </tab-bar>
</template>

<script>
import TabBar from 'components/common/tabbar/TabBar'
import TabBarItem from 'components/common/tabbar/TabBarItem'
export default {
    components: {
        TabBar,
        TabBarItem
    }
}
</script>

<style>

</style>