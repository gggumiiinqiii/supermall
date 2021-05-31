<template>
  <div id="home">
    <nav-bar class="home-nav">
      <template v-slot:center>购物街</template>
    </nav-bar>
    <swiper>
      <template v-slot:slideee>
        <swiper-item v-for="(item,index) in banners" :key="index">
        <template v-slot:slidename>
          <a :href="item.link">
          <img :src="item.image" alt="">
          </a>
        </template>
      </swiper-item>
      </template>
    </swiper>
  </div>
</template>

<script>
import NavBar from 'components/common/navbar/NavBar.vue'
import {Swiper,SwiperItem} from 'components/common/swiper'
import {getHomeMultidata,getHomeGoods} from 'network/home.js'
export default {

  data(){
    return {
      banners:[],
      recommends:[],
    }
  },
  methods:{
    async fetchHomeMultidata(){
      const res = await getHomeMultidata()
      // console.log(res)
      this.banners = res.data.banner.list
      this.recommends = res.data.recommend.list
    }
  },
  created(){
    console.log('home被创建')
    this.fetchHomeMultidata()
  },
  destroyed(){
    console.log('home被销毁')
  },
  components:{
    NavBar,
    Swiper,
    SwiperItem
  },
}
</script>

<style scoped>
.home-nav {
  background-color: var(--color-tint);
  color: #fff;
}
</style>>
