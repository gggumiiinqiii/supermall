<template>
  <div class="feature">
    <h2>今日优选</h2>
    <div class="feature-item" v-for="(item,index) in featuregoods" :key="index">
      <a href="#">
      <img :src="item.img" alt="">
      <div>{{item.title}}</div>
      </a>
    </div>
  </div>
</template>

<script>
export default {
  name:'FeatureView',
  data(){
    return {
      featuregoods:[{
        img:'https://s10.mogucdn.com/mlcdn/c45406/180913_036dli57aah85cb82l1jj722g887g_225x225.png',
        title:'霸街长袖群'
      },{
        img:'https://s10.mogucdn.com/mlcdn/c45406/180913_036dli57aah85cb82l1jj722g887g_225x225.png',
        title:'时尚赖人套装'
      },{
        img:'https://s10.mogucdn.com/mlcdn/c45406/180913_036dli57aah85cb82l1jj722g887g_225x225.png',
        title:'霸街长袖群'
      },{
        img:'https://s10.mogucdn.com/mlcdn/c45406/180913_036dli57aah85cb82l1jj722g887g_225x225.png',
        title:'时尚赖人套装'
      },{
        img:'https://s10.mogucdn.com/mlcdn/c45406/180913_036dli57aah85cb82l1jj722g887g_225x225.png',
        title:'霸街长袖群'
      },{
        img:'https://s10.mogucdn.com/mlcdn/c45406/180913_036dli57aah85cb82l1jj722g887g_225x225.png',
        title:'时尚赖人套装'
      },{
        img:'https://s10.mogucdn.com/mlcdn/c45406/180913_036dli57aah85cb82l1jj722g887g_225x225.png',
        title:'霸街长袖群'
      },{
        img:'https://s10.mogucdn.com/mlcdn/c45406/180913_036dli57aah85cb82l1jj722g887g_225x225.png',
        title:'时尚赖人套装'
      },]
    }
  }
}
</script>

<style scoped>
.feature {
  display: flex;
  width: 100%;
  flex-wrap: wrap;
  text-align: center;
}
h2 {
  width: 100%;
  margin: 10px 0 10px;
  font-weight: 400;
}
.feature img{
  width: 80%;
}
.feature-item {
  font-size: 14px;
  width: 25%;
  margin-bottom: 13px;
}
</style>>
