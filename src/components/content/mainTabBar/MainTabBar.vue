<template>
   <tab-bar>
      <tab-bar-item link="/home">
          <div slot="tabbar-icon">
            <img src="~assets/img/tabbar/home.svg" alt="">
          </div>
          <div slot="tabbar-icon-active">
            <img src="~assets/img/tabbar/home_active.svg" alt="">
          </div>
          <div slot="tabbar-text">首页</div>
      </tab-bar-item>
      <tab-bar-item link="/category">
          <div slot="tabbar-icon">
            <img src="~assets/img/tabbar/category.svg" alt="">
          </div>
          <div slot="tabbar-icon-active">
             <img src="~assets/img/tabbar/category_active.svg" alt="">
          </div>
          <div slot="tabbar-text">分类</div>
      </tab-bar-item>
      <tab-bar-item link="/cart">
          <div slot="tabbar-icon">
             <img src="~assets/img/tabbar/shopcart.svg" alt="">
          </div>
          <div slot="tabbar-icon-active">
             <img src="~assets/img/tabbar/shopcart_active.svg" alt="">
          </div>
          <div slot="tabbar-text">购物车</div>
      </tab-bar-item>
      <tab-bar-item link="/profile">
          <div slot="tabbar-icon">
             <img src="~assets/img/tabbar/profile.svg" alt="">
          </div>
          <div slot="tabbar-icon-active">
             <img src="~assets/img/tabbar/profile_active.svg" alt="">
          </div>
          <div slot="tabbar-text">我的</div>
      </tab-bar-item>
    </tab-bar>
</template>

<script>
import tabBarItem from "components/common/tabbar/TabBarIItem.vue"
import TabBar from "components/common/tabbar/TabBar.vue"
export default {
  components:{
    TabBar,
    tabBarItem
  }
}
</script>

<style>
   
</style>