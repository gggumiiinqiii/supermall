<template>
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
</template>

<script>
import {Swiper,SwiperItem} from 'components/common/swiper'
export default {
  props:{
    banners:{
      type:Array,
      default(){
        return []
      }
    }
  },
  components:{
    Swiper,
    SwiperItem
  }
}
</script>

<style>

</style>