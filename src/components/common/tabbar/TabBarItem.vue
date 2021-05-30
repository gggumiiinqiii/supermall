<template>
  <div class="tab-bar-item" @click="itemClick">
    <div v-if="!isActive">
      <slot name="itemimg"></slot>
    </div>
    <div v-else>
      <slot name="itemimg2"></slot>
    </div>
    <div :style="activeStyle">
      <slot name="itemtext"></slot>
    </div>
  </div>
</template>

<script>
export default {
  props:{
    path:String,
    activeColor:{
      type:String,
      default:'red'
    }
  },
  computed:{
    isActive(){
      // 如果没有这字符串出现就返回-1，就不是这个活跃就返回false
      //this.$route梵文当前路由
      return this.$route.path.indexOf(this.path) !=-1;
    },
    activeStyle() {
      //当前为true文字颜色就是
      return this.isActive?{color: this.activeColor}:{};
    }
  },
  methods:{
    itemClick(){
      //当前路由
     // console.log(this.$route.path)
      //需要跳转的路由
      //console.log(this.path)
      // 如果在当前页面就不进行跳转，
      if(this.$route.path.indexOf(this.path) == -1){
        this.$router.push(this.path).catch(err=>{
          console.log('路由切换问题ERROR')
        })
      }
    }
  }
}
</script>

<style>
.tab-bar-item {
  /* display:flex 只针对子标签，所以在<template #default>下面只能有一个 子标签，如果外层套了一层div，则无用 */
  flex: 1;
  text-align: center;
  height: 2.5rem;
  font-size: 0.64rem;
}
.tab-bar-item img {
  width: 1.024rem;
  height: 1.024rem;
  margin-top: 0.126rem;
  margin-bottom: 0.3rem;
  vertical-align: middle;
}
</style>