<template>
  <div id="recommend">
    <div v-for="(item, index) in recommends" :key="index" class="recommend-item">
      <a :href="item.link">
        <img :src="item.image" alt="">
        <div>{{item.title}}</div>
      </a>
    </div>
  </div>
</template>


<script>
export default {
  name: "HomeRecommend",
  props: {
    recommends: {
      type: Array,
      defalt() {
        return []
      }
    }
  }
}
</script>

<style scope>
  #recommend {
    display: flex;
    width: 100%;
    text-align: center;
    font-size: 12px;
    padding: 15px 0px 20px;
    border-bottom: 8px #eee solid;
  }
  .recommend-item {
    flex: 1;
  }
  .recommend-item img {
    width: 80px;
    height: 80px;
    margin-bottom: 10px;
  }
</style>
