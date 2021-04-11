<template>
  <div>
    <tab-bar>
      <template #default>
        <tab-bar-item path='/home'>
          <template #item-icon>
            <img src="@/assets/image/tabbar/home.svg" />
          </template>
          <template #item-icon-active>
            <img src="~assets/image/tabbar/home_active.svg" />
          </template>
          <template #item-text><div>首页</div></template>
        </tab-bar-item>
        <tab-bar-item path='/category'>
          <template #item-icon>
            <img src="~assets/image/tabbar/category.svg" />
          </template>
          <template #item-icon-active>
            <img src="~assets/image/tabbar/category_active.svg" />
          </template>
          <template #item-text><div>商品分类</div></template>
        </tab-bar-item>
        <tab-bar-item path='/shopcart'>
          <template #item-icon>
            <img src="~assets/image/tabbar/shopcart.svg" />
          </template>
          <template #item-icon-active>
            <img src="~assets/image/tabbar/shopcart_active.svg" />
          </template>
          <template #item-text><div>购物车</div></template>
        </tab-bar-item>
        <tab-bar-item path='/profile'>
          <template #item-icon>
            <img src="~assets/image/tabbar/profile.svg" />
          </template>
          <template #item-icon-active>
            <img src="~assets/image/tabbar/profile_active.svg" />
          </template>
          <template #item-text><div>我的</div></template>
        </tab-bar-item>
      </template>

    </tab-bar>

  </div>
</template>

<script>
import TabBar from "@/components/common/tabbar/TarBar.vue"
import TabBarItem from "@/components/common/tabbar/TarBarItem.vue"
export default {
  name: 'MainTabBar',
  components: {
    TabBar ,
    TabBarItem
  }
}
</script>
