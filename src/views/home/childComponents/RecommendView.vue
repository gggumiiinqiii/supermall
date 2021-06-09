<template>
  <div class="recommend">
    <div class="recommend-item" v-for="(item,index) in recommends" :key="index">
      <a :href="item.link">
        <img :src="item.image" alt="">
        <div class="recommend-title">{{item.title}}</div>
      </a>
    </div>
  </div>
</template>

<script>
export default {
  name:'RecommendView',
  props:{
    recommends:{
      type:Array,
      default(){
        return []
      }
    }
  }
}
</script>

<style >
.recommend {
  display: flex;
  margin-bottom: 15px;
  box-shadow: 0 15px 1px rgb(100 100 100 / 10%);

}
.recommend-item {
  /* 默认flex就为1 */
  flex: 1;
  padding:10px 0 20px 0px;
  text-align: center;
}
.recommend-item img {
  width: 80%;
}
.recommend-title {
  margin-top: 5px;
}
</style>>

