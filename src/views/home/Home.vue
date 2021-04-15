<template>
  <div id="home">
    <nav-bar class="home-nav"><template #center>购物街</template></nav-bar>
    <!-- 轮播图 -->
    <home-swiper :banners="banners"></home-swiper>
    <home-recommend :recommends="recommends"></home-recommend>

  </div>
</template>
<script>
import NavBar from "@/components/common/navbar/NavBar"
import HomeSwiper from '@/views/home/childComps/HomeSwiper'
import HomeRecommend from '@/views/home/childComps/HomeRecommend'
import {getHomeMultidata} from "@/network/home.js"

export default {
  name: "Home",
  components: {
    NavBar,
    HomeSwiper,
    HomeRecommend
  },
  data() {
    return {
      banners: [],
      recommends: []
    }
  },
  created() {
    getHomeMultidata().then(res => {
      this.banners = res.data.banner.list;
      this.recommends = res.data.recommend.list;
    })
  }
}
</script>

<style scope>
.home-nav {
  background-color: var(--color-tint);
  color: #fff;
  font-weight: 700;
  /* 为了在使用原生滚动时，导航栏不随着内容滚动 */
  /* position: fixed;
  top: 0;
  left: 0;
  right: 0;
  z-index: 9; */
}
</style>
